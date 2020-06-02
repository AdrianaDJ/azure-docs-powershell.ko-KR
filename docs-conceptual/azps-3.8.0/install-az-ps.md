---
title: PowerShellGet으로 Azure PowerShell 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.openlocfilehash: 9cc681a56270c0894348a0eb6789ded3fa294f54
ms.sourcegitcommit: 80c3188500fd174f5c5484302360ad87ace0fb9b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83554594"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="c47ed-103">Azure Powershell 설치</span><span class="sxs-lookup"><span data-stu-id="c47ed-103">Install Azure PowerShell</span></span>

<span data-ttu-id="c47ed-104">이 문서에서는 [PowerShellGet](/powershell/scripting/gallery/installing-psget)을 사용하여 Azure PowerShell 모듈을 설치하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="c47ed-105">이러한 지침은 Windows, macOS 및 Linux 플랫폼에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="c47ed-106">Azure PowerShell은 Azure [Cloud Shell](/azure/cloud-shell/overview)에서도 사용할 수 있으며, 이제 [Docker 이미지](azureps-in-docker.md)에도 미리 설치되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c47ed-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c47ed-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="c47ed-108">모든 플랫폼에서 Azure PowerShell과 함께 사용할 것을 권장하는 PowerShell 버전은 PowerShell 7.x 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="c47ed-109">Azure PowerShell은 모든 플랫폼에서 PowerShell 6.2.4 이상과 함께 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="c47ed-110">Windows에서는 PowerShell 5.1도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="c47ed-111">사용하는 운영 체제에 제공되는 [최신 버전의 PowerShell](/powershell/scripting/install/installing-powershell)을 설치하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-111">Installing the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system is recommended.</span></span> <span data-ttu-id="c47ed-112">PowerShell 6.2.4 이상에서 실행하는 경우 Azure PowerShell과 관련된 추가 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="c47ed-113">PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="c47ed-114">Windows의 PowerShell 5.1에서 Azure PowerShell을 사용하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="c47ed-115">[Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-115">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="c47ed-116">Windows 10 버전 1607 이상을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="c47ed-117">[.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="c47ed-118">최신 버전의 PowerShellGet이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="c47ed-119">**관리자 권한으로 실행**을 사용하여 PowerShell 5.1 세션을 시작하고 `Install-Module -Name PowerShellGet -AllowClobber -Force`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-119">Start a PowerShell 5.1 session using **Run as administrator** and run `Install-Module -Name PowerShellGet -AllowClobber -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="c47ed-120">Azure PowerShell 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="c47ed-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="c47ed-121">Windows에서 PowerShell 5.1용 AzureRM과 Az 모듈을 동시에 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="c47ed-122">시스템에서 AzureRM을 사용할 수 있도록 유지해야 하는 경우 PowerShell 6.2.4 이상용 Az 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="c47ed-123">기본 설치 방법은 PowerShellGet cmdlet을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="c47ed-124">현재 사용자에 대해서만 Az 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="c47ed-125">이는 추천되는 설치 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-125">This is the recommended installation scope.</span></span> <span data-ttu-id="c47ed-126">이 방법은 Windows, macOS 및 Linux 플랫폼에서 동일하게 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="c47ed-127">PowerShell 세션에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="c47ed-128">기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않으며 다음 프롬프트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet and you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="c47ed-129">설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="c47ed-130">시스템의 모든 사용자에 대해 모듈을 설치하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-130">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="c47ed-131">Windows에서 **관리자 권한으로 실행**을 사용하여 PowerShell 세션을 시작하거나 macOS 또는 Linux에서 `sudo` 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-131">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="c47ed-132">Az 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-132">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c47ed-133">이 모듈을 설치하면 갤러리의 모든 사용 가능한 Az PowerShell 모듈이 다운로드되고, cmdlet을 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-133">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="c47ed-134">오프라인 설치</span><span class="sxs-lookup"><span data-stu-id="c47ed-134">Install offline</span></span>

<span data-ttu-id="c47ed-135">일부 환경에서는 PowerShell 갤러리에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-135">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="c47ed-136">이러한 경우에도 다음 방법 중 하나를 사용하여 오프라인으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-136">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="c47ed-137">모듈을 네트워크의 다른 위치에 다운로드하여 이 모듈을 네트워크의 설치 원본으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-137">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="c47ed-138">이 방법을 사용하면 단일 서버 또는 파일 공유에서 PowerShell 모듈을 캐시하여 PowerShellGet을 사용하여 연결이 끊긴 시스템에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-138">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="c47ed-139">[로컬 PowerShellGet 리포지토리로 작업](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)을 통해 로컬 리포지토리를 설정하고 연결이 끊어진 시스템에 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-139">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="c47ed-140">네트워크에 연결된 컴퓨터에 [Azure PowerShell MSI](install-az-ps-msi.md)를 다운로드한 다음, PowerShell 갤러리에 액세스하지 않고 설치 관리자를 시스템에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-140">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="c47ed-141">MSI 설치 관리자는 Windows의 PowerShell 5.1에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-141">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="c47ed-142">[Save-Module](/powershell/module/PowershellGet/Save-Module)을 사용하여 모듈을 파일 공유에 저장하거나 다른 소스에 저장하고 다른 컴퓨터에 수동으로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-142">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="c47ed-143">문제 해결</span><span class="sxs-lookup"><span data-stu-id="c47ed-143">Troubleshooting</span></span>

<span data-ttu-id="c47ed-144">Azure PowerShell 모듈을 설치할 때 나타나는 몇 가지 일반적인 문제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-144">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="c47ed-145">여기에 나열되지 않은 문제가 발생하면 [GitHub에서 문제를 제출](https://github.com/azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-145">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="c47ed-146">프록시 연결 차단</span><span class="sxs-lookup"><span data-stu-id="c47ed-146">Proxy blocks connection</span></span>

<span data-ttu-id="c47ed-147">`Install-Module`에서 PowerShell 갤러리에 연결할 수 없다는 오류가 발생하면 프록시를 지원하고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-147">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="c47ed-148">운영 체제와 네트워크 환경에 따라 시스템 수준 프록시 구성에 대한 요구 사항이 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-148">Different operating systems and network environments have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="c47ed-149">프록시 설정 및 환경에 맞게 구성하는 방법에 대해서는 시스템 관리자에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-149">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="c47ed-150">PowerShell 자체는 이 프록시를 자동으로 사용하도록 구성되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-150">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="c47ed-151">PowerShell 5.1 이상에서는 다음 명령을 사용하여 프록시를 사용하도록 PowerShell 세션을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-151">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="c47ed-152">운영 체제 자격 증명이 올바르게 구성되면 이 구성에서 프록시를 통해 PowerShell 요청을 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-152">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="c47ed-153">이 설정이 세션 간에 유지되도록 하려면 명령을 [PowerShell 프로필](/powershell/module/microsoft.powershell.core/about/about_profiles)에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-153">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="c47ed-154">패키지를 설치하려면 프록시에서 다음 주소에 대한 HTTPS 연결을 허용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-154">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="c47ed-155">로그인</span><span class="sxs-lookup"><span data-stu-id="c47ed-155">Sign in</span></span>

<span data-ttu-id="c47ed-156">Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-156">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="c47ed-157">모듈 자동 로딩을 비활성화한 경우 `Import-Module -Name Az`을 사용하여 모듈을 수동으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-157">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="c47ed-158">모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-158">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="c47ed-159">모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-159">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="c47ed-160">PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-160">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="c47ed-161">Azure PowerShell 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="c47ed-161">Update the Azure PowerShell module</span></span>

<span data-ttu-id="c47ed-162">PowerShell 모듈을 업데이트하려면 모듈을 설치하는 데 사용한 것과 동일한 방법을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-162">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="c47ed-163">예를 들어 처음에 `Install-Module`을 사용한 경우 [Update-Module](/powershell/module/powershellget/update-module)을 사용하여 최신 버전을 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-163">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="c47ed-164">처음에 MSI 패키지를 사용한 경우 새 MSI 패키지를 다운로드하여 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-164">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="c47ed-165">PowerShellGet cmdlet은 MSI 패키지에서 설치된 모듈을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-165">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="c47ed-166">MSI 패키지는 PowerShellGet을 사용하여 설치한 모듈을 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-166">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="c47ed-167">PowershellGet을 사용하여 업데이트하는 데 문제가 있는 경우 **업데이트**하는 대신 **다시 설치**해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-167">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="c47ed-168">다시 설치는 설치와 동일한 방식으로 수행되지만 `-Force` 매개 변수를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-168">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="c47ed-169">MSI 기반 설치와 달리 PowerShellGet을 사용하여 설치하거나 업데이트해도 시스템에 있을 수 있는 이전 버전은 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-169">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="c47ed-170">시스템에서 이전 버전의 Azure PowerShell을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-170">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="c47ed-171">MSI 기반 설치에 대한 자세한 내용은 [MSI를 사용하여 Azure PowerShell 설치](install-az-ps-msi.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-171">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="c47ed-172">여러 버전의 Azure PowerShell 사용</span><span class="sxs-lookup"><span data-stu-id="c47ed-172">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="c47ed-173">Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-173">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="c47ed-174">여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-174">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="c47ed-175">Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-175">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="c47ed-176">모듈 버전이 두 개 이상인 경우 모듈 자동 로드 및 `Import-Module`이 기본적으로 최신 버전을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-176">If you have more than one version of the module installed, module autoload, and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="c47ed-177">`-RequiredVersion` 매개 변수를 사용하여 특정 버전의 `Az` 모듈을 설치하거나 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-177">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a><span data-ttu-id="c47ed-178">PowerShellGet에서 여러 리포지토리 사용</span><span class="sxs-lookup"><span data-stu-id="c47ed-178">Use multiple repositories with PowerShellGet</span></span>

<span data-ttu-id="c47ed-179">시스템의 PowerShellGet에 리포지토리를 추가하고 그 중 2개 이상에서 Az 모듈을 찾을 수 있는 경우 **Repository** 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c47ed-179">The **Repository** parameter is required if you have added additional repositories to PowerShellGet on your system and the Az module can be found in more than one of them.</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a><span data-ttu-id="c47ed-180">피드백 제공</span><span class="sxs-lookup"><span data-stu-id="c47ed-180">Provide feedback</span></span>

<span data-ttu-id="c47ed-181">버그가 Azure PowerShell에 있으면 [GitHub에서 문제를 제기](https://github.com/Azure/azure-powershell/issues)하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-181">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="c47ed-182">명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-182">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c47ed-183">다음 단계</span><span class="sxs-lookup"><span data-stu-id="c47ed-183">Next Steps</span></span>

<span data-ttu-id="c47ed-184">Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-184">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="c47ed-185">Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c47ed-185">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>