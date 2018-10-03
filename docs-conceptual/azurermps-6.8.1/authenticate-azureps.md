---
title: Azure PowerShell로 로그인
description: Azure PowerShell 사용자나 서비스 주체로 로그인 또는 Azure 리소스에 대한 관리 ID로 로그인하는 방법.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 2a118e1aa8b6755ef5769f44429427d22532780d
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560238"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="66d3b-103">Azure PowerShell로 로그인</span><span class="sxs-lookup"><span data-stu-id="66d3b-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="66d3b-104">Azure PowerShell에서는 여러 인증 방법을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="66d3b-105">가장 간단하게 시작하는 방법은 명령줄에서 대화형으로 로그인하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="66d3b-106">대화형으로 로그인</span><span class="sxs-lookup"><span data-stu-id="66d3b-106">Sign in interactively</span></span>

<span data-ttu-id="66d3b-107">대화형으로 로그인하려면 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="66d3b-108">실행되는 경우 이 cmdlet은 귀하의 Azure 계정과 연결된 이메일 주소와 암호를 묻는 대화 상자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="66d3b-109">이 인증은 현재 PowerShell 세션 동안 지속됩니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66d3b-110">Azure PowerShell 6.3.0부터는 Windows에 로그인이 유지되는 한, 여러 PowerShell 세션에서 자격 증명을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="66d3b-111">자세한 내용은 [영구 자격 증명](context-persistence.md)에 대한 아티클을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="66d3b-112">서비스 주체를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="66d3b-112">Sign in with a service principal</span></span>

<span data-ttu-id="66d3b-113">서비스 주체는 비대화형 Azure 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="66d3b-114">다른 사용자 계정과 마찬가지로 해당 권한은 Azure Active Directory를 사용하여 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="66d3b-115">서비스 주체에 필요한 권한만 부여하여 자동화 스크립트 보안을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="66d3b-116">Azure PowerShell에 사용할 서비스 주체를 생성하는 방법을 보려면 [Azure PowerShell을 사용하여 Azure 서비스 주체 만들기](create-azure-service-principal-azureps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66d3b-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="66d3b-117">서비스 주체로 로그인하려면 `Connect-AzureRmAccount` cmdlet `-ServicePrincipal`인수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="66d3b-118">또한 서비스 주체의 응용 프로그램 ID, 로그인 자격 증명 및 서비스 주체와 연결된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="66d3b-119">서비스 주체의 자격 증명을 적절한 개체로 가져오려면 [Get-credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="66d3b-120">이 cmdlet은 서비스 주체 사용자 ID와 암호를 입력하는 대화 상자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="66d3b-121">Azure 관리 서비스 ID를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="66d3b-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="66d3b-122">Azure 리소스에 대한 관리 ID는 Azure Active Directory의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="66d3b-123">로그인에 관리 ID 서비스 주체를 사용할 수 있으며, 다른 리소스에 액세스하려면 앱 전용 액세스 토큰이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="66d3b-124">관리 ID는 Azure 클라우드에서 실행 중인 가상 머신에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="66d3b-125">Azure 리소스의 관리 ID에 대한 자세한 내용은 [Azure VM에서 Azure 리소스에 대한 관리 ID를 사용하여 액세스 토큰을 획득하는 방법](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66d3b-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="66d3b-126">다른 클라우드로 로그인</span><span class="sxs-lookup"><span data-stu-id="66d3b-126">Sign in to another Cloud</span></span>

<span data-ttu-id="66d3b-127">Azure 클라우드 서비스는 지역 데이터 처리 규정을 준수하는 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-127">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="66d3b-128">지역별 클라우드의 계정에 대해 로그인할 때 `-Environment` 인수를 사용해서 환경을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-128">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="66d3b-129">예를 들어 계정이 중국 클라우드에 있는 경우:</span><span class="sxs-lookup"><span data-stu-id="66d3b-129">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="66d3b-130">다음 명령은 사용 가능한 환경 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="66d3b-130">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="66d3b-131">Azure 역할 기반 액세스를 관리하는 방법에 대해 알아보기</span><span class="sxs-lookup"><span data-stu-id="66d3b-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="66d3b-132">Azure에서 인증 및 구독 관리에 대한 자세한 내용은 [계정, 구독 및 관리 역할 관리](/azure/active-directory/role-based-access-control-configure)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66d3b-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="66d3b-133">역할 관리를 위한 Azure PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="66d3b-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="66d3b-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d3b-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="66d3b-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66d3b-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="66d3b-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d3b-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="66d3b-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66d3b-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="66d3b-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66d3b-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="66d3b-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66d3b-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="66d3b-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66d3b-140">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
