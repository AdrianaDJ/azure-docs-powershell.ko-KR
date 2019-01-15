---
title: Azure PowerShell을 사용하여 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 앱 또는 서비스의 서비스 주체를 만드는 방법을 알아봅니다.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594958"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="ed1c5-104">Azure PowerShell을 사용하여 Azure 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="ed1c5-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="ed1c5-105">Azure PowerShell을 사용하여 앱 또는 서비스를 관리하려는 경우 소유한 자격 증명 대신 AAD(Azure Active Directory) 서비스 주체에서 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="ed1c5-106">이 문서에서는 Azure PowerShell을 사용하여 보안 주체를 만드는 과정을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="ed1c5-107">서비스 주체란?</span><span class="sxs-lookup"><span data-stu-id="ed1c5-107">What is a service principal?</span></span>

<span data-ttu-id="ed1c5-108">Azure 서비스 주체는 특정 Azure 리소스에 액세스하기 위해 사용자가 만든 앱과 서비스, 자동화 도구에서 사용하는 보안 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="ed1c5-109">서비스 주체에 해당 작업과 관련된 특정 권한을 할당하여 더 나은 보안 제어를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="ed1c5-110">이는 일반적으로 변경할 수 있는 권한이 있는 일반 사용자 ID와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="ed1c5-111">고유한 사용 권한 수준 확인</span><span class="sxs-lookup"><span data-stu-id="ed1c5-111">Verify your own permission level</span></span>

<span data-ttu-id="ed1c5-112">먼저 Azure Active Directory와 Azure 구독에 대한 충분한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="ed1c5-113">Active Directory에서 앱을 만들고 서비스 주체에 역할을 할당할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="ed1c5-114">계정에 올바른 사용 권한이 있는지를 확인하는 가장 쉬운 방법은 포털을 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="ed1c5-115">[필요한 사용 권한 확인](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="ed1c5-116">앱의 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="ed1c5-116">Create a service principal for your app</span></span>

<span data-ttu-id="ed1c5-117">Azure 계정에 로그인하면 서비스 주체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="ed1c5-118">다음 방법 중 하나로 배포된 앱을 식별해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="ed1c5-119">다음 예제처럼 "MyDemoWebApp"와 같은 배포된 앱의 고유 이름</span><span class="sxs-lookup"><span data-stu-id="ed1c5-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="ed1c5-120">애플리케이션 ID, 배포된 앱, 서비스 또는 개체와 관련된 고유 GUID</span><span class="sxs-lookup"><span data-stu-id="ed1c5-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="ed1c5-121">애플리케이션에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="ed1c5-121">Get information about your application</span></span>

<span data-ttu-id="ed1c5-122">`Get-AzADApplication` cmdlet을 사용하여 애플리케이션에 대한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="ed1c5-123">애플리케이션의 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="ed1c5-123">Create a service principal for your application</span></span>

<span data-ttu-id="ed1c5-124">`New-AzADServicePrincipal` cmdlet을 사용하여 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="ed1c5-125">여기에서 `$servicePrincipal.Secret` 속성을 `Connect-AzAccount`에 대한 인수로 직접 사용하거나(서비스 주체를 사용하여 로그인 참조) 이 `SecureString`을 일반 텍스트 문자열로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="ed1c5-126">서비스 주체를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="ed1c5-126">Sign in using the service principal</span></span>

<span data-ttu-id="ed1c5-127">이제 제공한 `appId` 및 생성한 `password`를 사용하여 앱에 새로운 서비스 주체로 로그인할 수</span><span class="sxs-lookup"><span data-stu-id="ed1c5-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="ed1c5-128">있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-128">generated.</span></span> <span data-ttu-id="ed1c5-129">서비스 주체에 대한 테넌트 ID도 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="ed1c5-130">개인 자격 증명을 사용하여 Azure에 로그인하는 경우 테넌트 ID가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="ed1c5-131">서비스 주체로 로그인하려면 해당 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="ed1c5-132">로그인이 성공한 후 다음과 같은 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="ed1c5-133">축하합니다!</span><span class="sxs-lookup"><span data-stu-id="ed1c5-133">Congratulations!</span></span> <span data-ttu-id="ed1c5-134">이러한 자격 증명을 사용하여 앱을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="ed1c5-135">다음으로 서비스 주체의 사용 권한을 조정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="ed1c5-136">역할 관리</span><span class="sxs-lookup"><span data-stu-id="ed1c5-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="ed1c5-137">Azure 역할 기반 Access Control(RBAC)은 사용자 및 서비스 주체에 대한 역할을 정의하고 관리하기 위한 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="ed1c5-138">역할에는 그와 관련된 일련의 사용 권한이 있으며 여기서 주체가 읽고 액세스하고 쓰고 관리할 수 있는 리소스를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="ed1c5-139">RBAC와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="ed1c5-140">Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="ed1c5-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ed1c5-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="ed1c5-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ed1c5-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="ed1c5-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ed1c5-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="ed1c5-144">서비스 주체의 기본 역할은 **참가자**입니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="ed1c5-145">광범위한 사용 권한을 고려하면 Azure 서비스와 앱의 상호 작용의 범위에 따라 최상의 선택이 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="ed1c5-146">**읽기 권한자** 역할은 더 제한적이며 읽기 전용 앱의 경우에 좋은 선택이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="ed1c5-147">역할 관련 사용 권한에 대한 세부 정보를 보거나 Azure Portal을 통해 사용자 지정 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="ed1c5-148">이 예제에서는 **읽기 권한자** 역할을 이전 예제에 추가하고 **참가자** 역할을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="ed1c5-149">현재 할당된 역할을 보려면:</span><span class="sxs-lookup"><span data-stu-id="ed1c5-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="ed1c5-150">역할 관리를 위한 기타 Azure PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ed1c5-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="ed1c5-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ed1c5-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="ed1c5-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ed1c5-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="ed1c5-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ed1c5-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="ed1c5-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ed1c5-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="ed1c5-155">보안 주체의 자격 증명 변경</span><span class="sxs-lookup"><span data-stu-id="ed1c5-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="ed1c5-156">보안을 향상시키려면 사용 권한을 검토하고 암호를 정기적으로 업데이트하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="ed1c5-157">앱이 변경될 때 보안 자격 증명을 관리하고 수정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="ed1c5-158">예를 들어, 새 암호를 만들고 이전 암호를 제거하여 서비스 주체의 암호를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed1c5-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="ed1c5-159">서비스 주체의 새 암호 추가</span><span class="sxs-lookup"><span data-stu-id="ed1c5-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="ed1c5-160">서비스 주체의 자격 증명 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="ed1c5-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="ed1c5-161">서비스 주체에게서 이전 암호 제거</span><span class="sxs-lookup"><span data-stu-id="ed1c5-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="ed1c5-162">서비스 주체의 자격 증명 목록 확인</span><span class="sxs-lookup"><span data-stu-id="ed1c5-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="ed1c5-163">서비스 주체에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="ed1c5-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```