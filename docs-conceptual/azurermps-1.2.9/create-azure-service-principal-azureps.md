---
title: Azure PowerShell을 사용하여 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 앱 또는 서비스의 서비스 주체를 만드는 방법을 알아봅니다.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 138047e510b7cb1f45abafe66c2b82ebc31c2cd9
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819646"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="8e846-104">Azure PowerShell을 사용하여 Azure 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="8e846-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="8e846-105">Azure PowerShell을 사용하여 앱 또는 서비스를 관리하려는 경우 고유한 자격 증명 대신 AAD(Azure Active Directory) 서비스 주체에서 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="8e846-106">이 항목에서는 Azure PowerShell을 사용하여 보안 주체를 만드는 과정을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="8e846-107">Azure Portal을 통해 서비스 주체를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="8e846-108">자세한 내용은 [포털을 사용하여 리소스에 액세스할 수 있는 Active Directory 응용 프로그램 및 서비스 주체 만들기](/azure/azure-resource-manager/resource-group-create-service-principal-portal)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e846-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="8e846-109">'서비스 주체'란?</span><span class="sxs-lookup"><span data-stu-id="8e846-109">What is a 'service principal'?</span></span>

<span data-ttu-id="8e846-110">Azure 서비스 주체는 특정 Azure 리소스에 액세스하기 위해 사용자가 만든 앱, 서비스 및 자동화 도구에서 사용하는 보안 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="8e846-111">특정한 역할이 있는 '사용자 ID'(사용자 이름과 암호 또는 인증서)이며 엄격하게 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="8e846-112">일반 사용자 ID와 달리 특정 작업만을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="8e846-113">해당 관리 작업을 수행하는 데 필요한 최소 사용 권한 수준을 부여하는 경우 보안이 향상됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="8e846-114">고유한 사용 권한 수준 확인</span><span class="sxs-lookup"><span data-stu-id="8e846-114">Verify your own permission level</span></span>

<span data-ttu-id="8e846-115">먼저 Azure Active Directory와 Azure 구독에 대한 충분한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="8e846-116">특히, Active Directory에서 앱을 만들고 서비스 주체에 역할을 할당할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="8e846-117">계정에 적절한 사용 권한이 있는지를 확인하는 가장 쉬운 방법은 포털을 통하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="8e846-118">[포털에서 필요한 사용 권한 확인](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e846-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="8e846-119">앱의 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="8e846-119">Create a service principal for your app</span></span>

<span data-ttu-id="8e846-120">Azure 계정에 로그인하면 서비스 주체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="8e846-121">다음 방법 중 하나로 배포된 앱을 식별해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="8e846-122">다음 예제에서 "MyDemoWebApp"와 같은 배포된 앱의 고유 이름 또는</span><span class="sxs-lookup"><span data-stu-id="8e846-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="8e846-123">응용 프로그램 ID, 배포된 앱, 서비스 또는 개체와 관련된 고유 GUID</span><span class="sxs-lookup"><span data-stu-id="8e846-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="8e846-124">응용 프로그램에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e846-124">Get information about your application</span></span>

<span data-ttu-id="8e846-125">`Get-AzureRmADApplication` cmdlet을 사용하여 응용 프로그램에 대한 정보를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="8e846-126">응용 프로그램의 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="8e846-126">Create a service principal for your application</span></span>

<span data-ttu-id="8e846-127">`New-AzureRmADServicePrincipal` cmdlet을 사용하여 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="8e846-128">서비스 주체에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e846-128">Get information about the service principal</span></span>

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="8e846-129">서비스 주체를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="8e846-129">Sign in using the service principal</span></span>

<span data-ttu-id="8e846-130">이제 제공한 *appId* 및 *암호*를 사용하여 앱에 새로운 서비스 주체로 로그인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="8e846-131">계정에 테넌트 ID를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="8e846-132">개인 자격 증명을 사용하여 Azure에 로그인하는 경우 테넌트 ID가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="8e846-133">새 PowerShell 세션에서 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="8e846-134">성공적으로 로그인한 후에 다음과 같은 출력이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-134">After a successfully signing on you see output something like this:</span></span>

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="8e846-135">축하합니다!</span><span class="sxs-lookup"><span data-stu-id="8e846-135">Congratulations!</span></span> <span data-ttu-id="8e846-136">이러한 자격 증명을 사용하여 앱을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="8e846-137">다음으로 서비스 주체의 사용 권한을 조정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="8e846-138">역할 관리</span><span class="sxs-lookup"><span data-stu-id="8e846-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="8e846-139">Azure 역할 기반 Access Control(RBAC)은 사용자 및 서비스 주체에 대한 역할을 정의하고 관리하기 위한 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="8e846-140">역할에는 그와 관련된 일련의 사용 권한이 있으며 여기서 주체가 읽고 액세스하고 쓰고 관리할 수 있는 리소스를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="8e846-141">RBAC와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e846-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="8e846-142">Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="8e846-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e846-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="8e846-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e846-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="8e846-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8e846-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="8e846-146">서비스 주체의 기본 역할은 **참가자**입니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="8e846-147">광범위한 사용 권한을 고려하면 Azure 서비스와 앱의 상호 작용의 범위에 따라 최상의 선택이 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="8e846-148">**판독기** 역할은 더 제한적이며 읽기 전용 앱의 경우에 좋은 선택이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="8e846-149">역할 관련 사용 권한에 대한 세부 정보를 보거나 Azure Portal을 통해 사용자 지정 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="8e846-150">이 예제에서는 **판독기** 역할을 이전 예제에 추가하고 **참가자** 역할을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="8e846-151">현재 할당된 역할을 보려면:</span><span class="sxs-lookup"><span data-stu-id="8e846-151">To view the current roles assigned:</span></span>

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="8e846-152">역할 관리를 위한 기타 Azure PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8e846-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="8e846-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8e846-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="8e846-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8e846-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="8e846-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8e846-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="8e846-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8e846-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="8e846-157">보안 주체의 자격 증명 변경</span><span class="sxs-lookup"><span data-stu-id="8e846-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="8e846-158">사용 권한을 검토하고 암호를 정기적으로 업데이트하는 좋은 보안 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="8e846-159">앱이 변경되면 보안 자격 증명을 관리하고 수정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="8e846-160">예를 들어, 새 암호를 만들고 이전 암호를 제거하여 서비스 주체의 암호를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e846-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="8e846-161">서비스 주체의 새 암호 추가</span><span class="sxs-lookup"><span data-stu-id="8e846-161">Add a new password for the service principal</span></span>

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="8e846-162">서비스 주체의 자격 증명 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e846-162">Get a list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="8e846-163">서비스 주체에게서 이전 암호 제거</span><span class="sxs-lookup"><span data-stu-id="8e846-163">Remove the old password from the service principal</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="8e846-164">서비스 주체의 자격 증명 목록 확인</span><span class="sxs-lookup"><span data-stu-id="8e846-164">Verify the list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
