---
title: "Azure PowerShell Service Management 모듈 설치 및 구성 | Microsoft Docs"
description: "Azure PowerShell을 처음으로 설치하고 구성하는 방법입니다."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: f46fe25352c100976dd8fc3b1c48ddfc3926f906
ms.sourcegitcommit: 7a1c08518b180de822c915db99b055b93a1459d7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2017
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="6d0fe-103">Azure PowerShell Service Management 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="6d0fe-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="6d0fe-104">[PowerShell 갤러리](https://www.powershellgallery.com/)에서 Azure PowerShell을 설치하는 것이 기본적인 설치 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="6d0fe-105">1단계: PowerShellGet 설치</span><span class="sxs-lookup"><span data-stu-id="6d0fe-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="6d0fe-106">PowerShell 갤러리에서 항목을 설치하려면 PowerShellGet 모듈이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="6d0fe-107">적절한 버전의 PowerShellGet 및 다른 시스템 요구 사항이 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="6d0fe-108">PowerShellGet이 시스템에 설치되어 있는지 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="6d0fe-109">다음과 비슷하게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="6d0fe-110">PowerShellGet을 설치하지 않은 경우 [PowerShellGet을 가져오는 방법](#how-to-get-powershellget)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="6d0fe-111">2단계: Azure PowerShell 설치</span><span class="sxs-lookup"><span data-stu-id="6d0fe-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="6d0fe-112">관리자 권한으로 실행하는 Windows PowerShell 콘솔에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="6d0fe-113">Azure 모듈은 Azure Resource Manager cmdlet의 롤업 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="6d0fe-114">AzureRM 모듈을 설치하는 경우 이전에 설치되지 않은 다른 Azure 모듈을 PowerShell 갤러리에서 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="6d0fe-115">Azure Service Management 모듈은 Azure PowerShell Resource Manager 모듈을 사용하여 종속성을 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="6d0fe-116">Azure PowerShell Resource Manager 모듈을 설치한 경우 `-AllowClobber` 매개 변수를 설치 명령에 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="6d0fe-117">이렇게 하면 이 기존 공유 종속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="6d0fe-118">이 매개 변수가 없으면 모듈을 설치하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="6d0fe-119">이 모듈을 설치한 후에 다음 명령을 실행하여 모듈을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="6d0fe-120">cmdlet을 사용하려면</span><span class="sxs-lookup"><span data-stu-id="6d0fe-120">To use the cmdlets</span></span>

<span data-ttu-id="6d0fe-121">Azure Service Management cmdlet을 사용하려면 먼저 Azure 계정에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="6d0fe-122">계정에 로그인하려면 이제 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="6d0fe-123">Azure PowerShell에서는 Azure에 로그인한 후에 지정된 세션에 대한 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="6d0fe-124">해당 컨텍스트는 해당 세션 내에서 모든 cmdlet에 사용할 Azure PowerShell 환경, 계정, 테넌트 및 구독을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="6d0fe-125">이제 아래의 모듈을 사용할 준비가 완료되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="6d0fe-126">Azure Service Management cmdlet</span><span class="sxs-lookup"><span data-stu-id="6d0fe-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="6d0fe-127">Azure PowerShell 모듈은 자주 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="6d0fe-128">모듈에 있지 않은 cmdlet 또는 매개 변수가 온라인 cmdlet 도움말에 포함되는 경우 최신 버전의 모듈을 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="6d0fe-129">모듈의 버전을 찾으려면 `(Get-Module Azure).Version`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="6d0fe-130">Azure에서 일반적인 일부 작업을 자동화할 수 있는 샘플 스크립트는 [Windows Azure 스크립트 센터](http://www.windowsazure.com/documentation/scripts/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="6d0fe-131">Windows PowerShell을 설치, 학습, 사용 및 사용자 지정하는 방법에 대한 일반적인 정보는 [Windows PowerShell을 사용하여 스크립팅](http://go.microsoft.com/fwlink/p/?linkid=320210)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="6d0fe-132">PowerShellGet을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="6d0fe-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="6d0fe-133">OS 버전</span><span class="sxs-lookup"><span data-stu-id="6d0fe-133">OS Version</span></span>|<span data-ttu-id="6d0fe-134">설치 지침</span><span class="sxs-lookup"><span data-stu-id="6d0fe-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="6d0fe-135">Windows 10 또는 Windows Server 2016을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="6d0fe-136">OS에 포함된 WMF(Windows Management Framework) 5.0으로 빌드됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="6d0fe-137">PowerShell 5로 업그레이드하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="6d0fe-138">최신 버전의 WMF 설치</span><span class="sxs-lookup"><span data-stu-id="6d0fe-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="6d0fe-139">PowerShell 3 또는 PowerShell 4를 사용하는 Windows 버전에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="6d0fe-140">PackageManagement 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="6d0fe-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="6d0fe-141">Azure PowerShell 버전 확인</span><span class="sxs-lookup"><span data-stu-id="6d0fe-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="6d0fe-142">가능한 한 빨리 최신 버전으로 업그레이드하는 것이 좋지만 여러 버전의 Azure PowerShell이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="6d0fe-143">설치한 Azure PowerShell의 버전을 확인하려면 명령줄에서 `Get-Module AzureRM`을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
