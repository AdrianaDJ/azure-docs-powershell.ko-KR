---
title: Azure PowerShell 제거
description: Azure PowerShell의 전체 제거를 수행하는 방법
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: eaabd8014368f7ea8f4c9504e58d920dad8a6518
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498627"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="e6c4e-103">Azure PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="e6c4e-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="e6c4e-104">이 문서에서는 Azure PowerShell의 이전 버전을 제거하거나 시스템에서 완전히 제거하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="e6c4e-105">Azure PowerShell을 완전히 제거하기로 한 경우 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 통해 몇 가지 피드백을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="e6c4e-106">버그가 발생하면 해결을 위해 [GitHub 문제를 제출](https://github.com/azure/azure-powershell/issues)해 주시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="e6c4e-107">Az 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="e6c4e-107">Uninstall the Az module</span></span>

<span data-ttu-id="e6c4e-108">Az 모듈을 제거하려면 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="e6c4e-109">그러나 `Uninstall-Module`은 모듈 중 하나만 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="e6c4e-110">Azure PowerShell을 완전히 제거하려면 각 모듈을 개별적으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="e6c4e-111">2개 이상의 Azure PowerShell 버전을 설치한 경우 제거가 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="e6c4e-112">현재 설치한 Azure PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="e6c4e-113">다음 스크립트는 PowerShell 갤러리를 쿼리하여 종속 하위 모듈의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="e6c4e-114">그런 다음 스크립트는 올바른 버전의 각 하위 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="e6c4e-115">`Process` 또는 `CurrentUser`외의 범위에서 이 스크립트를 실행하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="e6c4e-116">이 함수를 사용하려면 코드를 복사하고 PowerShell 세션에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="e6c4e-117">다음 예제에서는 이전 버전의 Azure PowerShell을 제거하는 함수를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="e6c4e-118">이 스크립트를 실행하면 제거하고 있는 각 하위 모듈의 이름 및 버전이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="e6c4e-119">제거하지는 안되, 삭제할 것을 표시만 하도록 스크립트를 실행하려면 `-WhatIf` 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="e6c4e-120">제거하려는 Azure PowerShell의 모든 버전에 대해 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="e6c4e-121">편의를 위해, 다음 스크립트는 최신 버전을 __제외한__ 모든 Az 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="e6c4e-122">AzureRM 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="e6c4e-123">시스템에 Az 모듈이 설치되어 있고 AzureRM을 제거하려면 위의 `Uninstall-AllModules` 스크립트를 실행하지 않아도 되는 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="e6c4e-124">수행할 방법은 AzureRM 모듈을 설치한 방법에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="e6c4e-125">원래의 설치 방법을 잘 모르는 경우 먼저 MSI를 제거하는 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-125">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="e6c4e-126">Azure PowerShell MSI 제거</span><span class="sxs-lookup"><span data-stu-id="e6c4e-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="e6c4e-127">MSI 패키지를 사용하여 Azure PowerShell AzureRM 모듈을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="e6c4e-128">플랫폼</span><span class="sxs-lookup"><span data-stu-id="e6c4e-128">Platform</span></span> | <span data-ttu-id="e6c4e-129">지침</span><span class="sxs-lookup"><span data-stu-id="e6c4e-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="e6c4e-130">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="e6c4e-130">Windows 10</span></span> | <span data-ttu-id="e6c4e-131">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="e6c4e-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="e6c4e-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6c4e-132">Windows 7</span></span> </br><span data-ttu-id="e6c4e-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6c4e-133">Windows 8</span></span> | <span data-ttu-id="e6c4e-134">시작>제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="e6c4e-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="e6c4e-135">이 화면을 띄우면 프로그램 목록에 __Azure PowerShell__이 보일 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="e6c4e-136">이 앱을 제거하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-136">This is the app to uninstall.</span></span> <span data-ttu-id="e6c4e-137">이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="e6c4e-138">PowerShell에서 제거하기</span><span class="sxs-lookup"><span data-stu-id="e6c4e-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="e6c4e-139">AzureRM을 PowerShellGet과 함께 설치한 경우 `Az.Accounts` 모듈의 일부로 사용할 수 있는 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) 명령을 사용하여 모듈을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="e6c4e-140">이는 컴퓨터에서 _모든_ AzureRM 모듈을 제거할 수 있지만 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="e6c4e-141">`Uninstall-AzureRM` 명령을 성공적으로 실행할 수 없으면 이 문서에서 제공하는 [`Uninstall-AllModules` 스크립트](#uninstall-script)를 사용하여 다음과 같이 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c4e-141">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```