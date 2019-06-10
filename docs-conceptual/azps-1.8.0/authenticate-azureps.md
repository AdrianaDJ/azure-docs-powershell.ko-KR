---
title: Azure PowerShell로 로그인
description: Azure PowerShell 사용자나 서비스 주체로 로그인 또는 Azure 리소스에 대한 관리 ID로 로그인하는 방법.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 1e25d4650cc20d7b6613e0efb12ec60d424608c4
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66375739"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ab02d-103">Azure PowerShell로 로그인</span><span class="sxs-lookup"><span data-stu-id="ab02d-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="ab02d-104">Azure PowerShell에서는 여러 인증 방법을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="ab02d-105">시작하는 가장 쉬운 방법은 [Azure Cloud Shell](/azure/cloud-shell/overview)을 사용하는 것으로서, 자동으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="ab02d-106">로컬 설치에서는, 브라우저를 통해 대화형으로 로그인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="ab02d-107">자동화 스크립트를 작성할 때 권장되는 방법은 필요한 권한이 있는 [서비스 주체](create-azure-service-principal-azureps.md)를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="ab02d-108">사용 사례에 대해 로그인 권한을 가능한 한 많이 제한하면 Azure 리소스를 안전하게 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="ab02d-109">로그인한 후 명령은 기본 구독에 대해 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="ab02d-110">세션에 대한 활성 구독을 변경하려면 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="ab02d-111">Azure PowerShell로 로그인할 때 사용되는 기본 구독을 변경하려면 [Set-AzDefault](/powershell/module/az.accounts/set-azdefault)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ab02d-112">로그인한 상태를 유지하는 한, 여러 PowerShell 세션에서 자격 증명을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="ab02d-113">자세한 내용은 [영구 자격 증명](context-persistence.md)에 대한 아티클을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ab02d-114">대화형으로 로그인</span><span class="sxs-lookup"><span data-stu-id="ab02d-114">Sign in interactively</span></span>

<span data-ttu-id="ab02d-115">대화형으로 로그인하려면 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="ab02d-116">실행되면 이 cmdlet은 토큰 문자열을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="ab02d-117">로그인 하려면 이 문자열을 복사하여 브라우저에서 https://microsoft.com/devicelogin에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="ab02d-118">그러면 PowerShell 세션이 인증되어 Azure에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ab02d-119">Active Directory Domain Services 인증 구현 및 보안 문제의 변경으로 인해 Azure PowerShell에서 사용자 이름/암호 자격 증명이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="ab02d-120">자동화 목적으로 자격 증명 권한 부여를 사용하는 경우 대신 [서비스 주체](create-azure-service-principal-azureps.md)를 생성하세요.</span><span class="sxs-lookup"><span data-stu-id="ab02d-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="ab02d-121">서비스 주체 <a name="sp-signin"/>으로 로그인</span><span class="sxs-lookup"><span data-stu-id="ab02d-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="ab02d-122">서비스 주체는 비대화형 Azure 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="ab02d-123">다른 사용자 계정과 마찬가지로 해당 권한은 Azure Active Directory를 사용하여 관리됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="ab02d-124">서비스 주체에 필요한 권한만 부여하여 자동화 스크립트 보안을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="ab02d-125">Azure PowerShell에 사용할 서비스 주체를 생성하는 방법을 보려면 [Azure PowerShell을 사용하여 Azure 서비스 주체 만들기](create-azure-service-principal-azureps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ab02d-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ab02d-126">서비스 주체로 로그인하려면 `Connect-AzAccount` cmdlet `-ServicePrincipal`인수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="ab02d-127">또한 서비스 주체의 애플리케이션 ID, 로그인 자격 증명 및 서비스 주체와 연결된 테넌트 ID가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="ab02d-128">서비스 보안 주체로 로그인하는 방법은 암호 기반 또는 인증서 기반 인증 중 어떤 것으로 구성되어 있는지에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="ab02d-129">암호 기반 인증</span><span class="sxs-lookup"><span data-stu-id="ab02d-129">Password-based authentication</span></span>

<span data-ttu-id="ab02d-130">서비스 주체의 자격 증명을 적절한 개체로 가져오려면 [Get-credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ab02d-131">이 cmdlet에는 사용자 이름 및 암호를 요청하는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="ab02d-132">사용자 이름에 대한 서비스 주체 ID를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="ab02d-133">자동화 시나리오의 경우 사용자 이름 및 보안 문자열에서 자격 증명을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="ab02d-134">서비스 주체 연결을 자동화할 때 좋은 암호 스토리지 방법을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="ab02d-135">인증서 기반 인증</span><span class="sxs-lookup"><span data-stu-id="ab02d-135">Certificate-based authentication</span></span>

<span data-ttu-id="ab02d-136">인증서 기반 인증을 사용하려면 Azure PowerShell이 인증서 지문을 기반으로 로컬 인증서 저장소에서 정보를 검색할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="ab02d-137">PowerShell 5.1에서 인증서 저장소는 [PKI](/powershell/module/pkiclient) 모듈을 사용하여 관리하고 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-137">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="ab02d-138">PowerShell Core 6.x 이상에서는 프로세스가 더 복잡합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-138">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="ab02d-139">다음 스크립트는 기존 인증서를 PowerShell에서 액세스할 수 있는 인증서 저장소로 가져오는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="ab02d-140">PowerShell 5.1에서 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="ab02d-140">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="ab02d-141">PowerShell Core 6.x 이상에서 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="ab02d-141">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="ab02d-142">관리 ID를 사용하여 로그인</span><span class="sxs-lookup"><span data-stu-id="ab02d-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="ab02d-143">관리 ID는 Azure Active Directory의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="ab02d-144">관리 ID는 Azure에서 실행되는 리소스에 할당된 서비스 주체입니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="ab02d-145">로그인에 관리 ID 서비스 주체를 사용할 수 있으며, 다른 리소스에 액세스하려면 앱 전용 액세스 토큰이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ab02d-146">관리 ID는 Azure 클라우드에서 실행되는 리소스에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="ab02d-147">Azure 리소스의 관리 ID에 대한 자세한 내용은 [Azure VM에서 Azure 리소스에 대한 관리 ID를 사용하여 액세스 토큰을 획득하는 방법](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ab02d-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="ab02d-148">기본이 아닌 테넌트를 사용하여 로그인하거나 클라우드 솔루션 공급자(CSP)로 로그인</span><span class="sxs-lookup"><span data-stu-id="ab02d-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="ab02d-149">계정이 둘 이상의 테넌트와 연결되어 있는 경우 로그인은 연결 시 `-TenantId` 매개 변수를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="ab02d-150">이 매개 변수는 다른 로그인 메서드를 사용하여 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="ab02d-151">로그인할 때 이 매개 변수 값은 테넌트의 Azure 개체 ID(테넌트 ID) 또는 테넌트의 정규화된 도메인 이름이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="ab02d-152">[클라우드 솔루션 공급자(CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/)의 경우 `-TenantId` 값은 **반드시** 테넌트 ID여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ab02d-153">다른 클라우드로 로그인</span><span class="sxs-lookup"><span data-stu-id="ab02d-153">Sign in to another Cloud</span></span>

<span data-ttu-id="ab02d-154">Azure 클라우드 서비스는 지역 데이터 처리법을 준수하는 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="ab02d-155">지역별 클라우드의 계정에 대해 로그인할 때 `-Environment` 인수를 사용해서 환경을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="ab02d-156">예를 들어 계정이 중국 클라우드에 있는 경우:</span><span class="sxs-lookup"><span data-stu-id="ab02d-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ab02d-157">다음 명령은 사용 가능한 환경 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab02d-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```