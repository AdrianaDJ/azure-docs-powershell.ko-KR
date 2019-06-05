---
title: Microsoft Azure PowerShell 5.0.0의 주요 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell 버전 5 릴리스에 이루어진 호환성이 손상되는 변경의 목록이 포함되어 있습니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534598"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="a4e68-103">Microsoft Azure PowerShell 5.0.0의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="a4e68-104">이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a4e68-105">각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="a4e68-106">심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="a4e68-107">목차</span><span class="sxs-lookup"><span data-stu-id="a4e68-107">Table of Contents</span></span>

- [<span data-ttu-id="a4e68-108">ApiManagement cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="a4e68-109">Batch cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="a4e68-110">Compute cmdlet의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="a4e68-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="a4e68-111">EventHub cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="a4e68-112">Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="a4e68-113">Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="a4e68-114">Resources cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="a4e68-115">ServiceBus cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="a4e68-116">ApiManagement cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="a4e68-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="a4e68-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="a4e68-118">매개 변수 "UserName" 및 "Password"가 PSCredential에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="a4e68-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="a4e68-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="a4e68-120">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="a4e68-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="a4e68-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="a4e68-122">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="a4e68-123">Batch cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="a4e68-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="a4e68-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="a4e68-125">매개 변수 `Password`가 보안 문자열에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="a4e68-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="a4e68-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="a4e68-127">매개 변수 `Password`가 보안 문자열에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="a4e68-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="a4e68-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="a4e68-129">매개 변수 `Password`가 보안 문자열에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="a4e68-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="a4e68-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="a4e68-131">`RunElevated` 스위치가 제거되고 `UserIdentity`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="a4e68-132">또한 `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` 및 `PSJobReleaseTask`의 `RunElevated` 속성에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="a4e68-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="a4e68-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="a4e68-134">`PSMultiInstanceSettings` 생성자는 더 이상 필수 `numberOfInstances` 매개 변수를 사용하지 않고 대신 필수 `coordinationCommandLine` 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="a4e68-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="a4e68-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="a4e68-136">`PSCloudTask`에서 `RunElevated` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="a4e68-137">`UserIdentity`를 대체하기 위해 `RunElevated` 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="a4e68-138">또한 `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` 및 `PSJobReleaseTask`의 `RunElevated` 속성에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="a4e68-139">**여러 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-139">**Multiple types**</span></span>

- <span data-ttu-id="a4e68-140">`PSExitConditions`에서 `SchedulingError` 속성의 이름이 `PreProcessingError`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="a4e68-141">**여러 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-141">**Multiple types**</span></span>

- <span data-ttu-id="a4e68-142">`PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` 및 `PSTaskExecutionInformation`에서 `SchedulingError` 속성의 이름이 `FailureInformation`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="a4e68-143">작업 실패가 있을 때마다 `FailureInformation`이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="a4e68-144">여기에는 이전의 모든 예약 오류 사례는 물론, 0이 아닌 작업 종료 코드 및 새 출력 파일 기능의 파일 업로드 오류가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="a4e68-145">이것은 이전과 동일하게 구성되므로 이 형식을 사용할 때는 코드 변경 내용이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="a4e68-146">또한 이것은 다음에 영향을 줍니다. Get-AzureBatchPool, Get-AzureBatchSubtask, Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="a4e68-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="a4e68-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="a4e68-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="a4e68-148">`TargetDedicated`가 제거되고 `TargetDedicatedComputeNodes` 및 `TargetLowPriorityComputeNodes`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="a4e68-149">`TargetDedicatedComputeNodes`에 `TargetDedicated` 별칭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="a4e68-150">또한 이것은 다음에 영향을 줍니다. Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="a4e68-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="a4e68-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="a4e68-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="a4e68-152">`PSCloudPool`에서 `TargetDedicated` 및 `CurrentDedicated` 속성 이름이 `TargetDedicatedComputeNodes` 및 `CurrentDedicatedComputeNodes`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="a4e68-153">**PSCloudPool 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="a4e68-154">`PSCloudPool`에서 `ResizeError`의 이름이 `ResizeErrors`로 변경되었고 이제 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="a4e68-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="a4e68-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="a4e68-156">`PSPoolSpecification`에서 `TargetDedicated` 속성의 이름이 `TargetDedicatedComputeNodes`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="a4e68-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="a4e68-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="a4e68-158">`Name`이 제거되고 `Path`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="a4e68-159">`Path`에 `Name` 별칭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="a4e68-160">또한 이것은 다음에 영향을 줍니다. Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="a4e68-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="a4e68-161">**PSNodeFile** 형식</span><span class="sxs-lookup"><span data-stu-id="a4e68-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="a4e68-162">`PSNodeFile`에서 `Name` 속성의 이름이 `Path`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="a4e68-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="a4e68-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="a4e68-164">`PSSubtaskInformation`의 `PreviousState` 및 `State` 속성은 더 이상 `TaskState` 형식이 아니며, 대신 `SubtaskState` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="a4e68-165">하위 작업이 `Active` 상태가 될 수 없으므로, `TaskState`와 달리, `SubtaskState`에는 `Active` 값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="a4e68-166">Compute cmdlet의 호환성이 손상되는 변경</span><span class="sxs-lookup"><span data-stu-id="a4e68-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="a4e68-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="a4e68-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="a4e68-168">매개 변수 "UserName" 및 "Password"가 PSCredential에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="a4e68-169">EventHub cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-171">'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-172">'New-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-174">'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-175">'Get-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-177">'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-178">'Set-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-180">'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-181">'Remove-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="a4e68-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="a4e68-183">'New-AzureRmEventHubNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-184">'New-AzureRmEventHubKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="a4e68-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="a4e68-186">'Get-AzureRmEventHubNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-187">'Get-AzureRmEventHubKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="a4e68-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="a4e68-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="a4e68-189">NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="a4e68-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="a4e68-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="a4e68-191">NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="a4e68-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="a4e68-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="a4e68-193">NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="a4e68-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="a4e68-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="a4e68-195">ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="a4e68-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="a4e68-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="a4e68-197">ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="a4e68-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="a4e68-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="a4e68-199">ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="a4e68-200">Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="a4e68-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="a4e68-202">**Add-AzureRMLogAlertRule** cmdlet이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="a4e68-203">이 cmdlet을 사용하는 10월 1일 이후에는 이 기능이 활동 로그 경고로 전환되므로 더 이상 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="a4e68-204">자세한 내용은 https://aka.ms/migratemealerts을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="a4e68-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="a4e68-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="a4e68-206">**Get-AzureRMUsage** cmdlet이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="a4e68-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="a4e68-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="a4e68-208">출력 변경: 이제 상수 값(Admin,Operation)을 반환하므로 EventData 개체(이러한 cmdlet에서 반환됨)의 EventChannels 필드가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="a4e68-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="a4e68-210">출력 변경: 이 cmdlet의 출력이 평면화되어, 즉 속성 필드가 제거되어 사용자 환경이 개선될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="a4e68-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="a4e68-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="a4e68-212">출력 변경: AutoscaleSettingResourceName 필드는 항상 이름 필드와 같으므로 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="a4e68-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="a4e68-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="a4e68-214">출력 변경: 출력 형식은 요청 ID 및 상태 코드가 포함된 단일 개체를 반환하도록 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="a4e68-215">Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="a4e68-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="a4e68-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="a4e68-217">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="a4e68-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="a4e68-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="a4e68-219">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="a4e68-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="a4e68-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="a4e68-221">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="a4e68-222">Resources cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="a4e68-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="a4e68-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="a4e68-224">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="a4e68-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="a4e68-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="a4e68-226">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="a4e68-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="a4e68-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="a4e68-228">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="a4e68-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="a4e68-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="a4e68-230">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="a4e68-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="a4e68-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="a4e68-232">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="a4e68-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="a4e68-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="a4e68-234">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="a4e68-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="a4e68-235">ServiceBus cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="a4e68-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a4e68-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-237">'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-238">'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="a4e68-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="a4e68-240">'Get-AzureRmServiceBusTopicKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-241">'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a4e68-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-243">'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-244">'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="a4e68-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="a4e68-246">'New-AzureRmServiceBusTopicKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-247">'New-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a4e68-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-249">'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-250">'Remove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="a4e68-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-252">'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-253">'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="a4e68-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="a4e68-255">'New-AzureRmServiceBusNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-256">'New-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a4e68-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-258">'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-259">'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="a4e68-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="a4e68-261">'Get-AzureRmServiceBusQueueKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-262">'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a4e68-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-264">'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-265">'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="a4e68-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="a4e68-267">'New-AzureRmServiceBusQueueKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-268">'New-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a4e68-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-270">'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-271">'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="a4e68-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-273">'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-274">'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-276">'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-277">'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="a4e68-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="a4e68-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="a4e68-279">'Get-AzureRmServiceBusNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-280">'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-282">'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-283">'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-285">'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-286">'Remove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="a4e68-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="a4e68-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="a4e68-288">'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="a4e68-289">'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4e68-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="a4e68-290">**NamespaceAttributes 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="a4e68-291">다음 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-291">The following properties have been removed</span></span>
    - <span data-ttu-id="a4e68-292">사용</span><span class="sxs-lookup"><span data-stu-id="a4e68-292">Enabled</span></span>
    - <span data-ttu-id="a4e68-293">상태</span><span class="sxs-lookup"><span data-stu-id="a4e68-293">Status</span></span>
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="a4e68-294">**QueueAttribute 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="a4e68-295">다음 속성은 사용되지 않음으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="a4e68-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="a4e68-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="a4e68-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="a4e68-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="a4e68-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="a4e68-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="a4e68-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="a4e68-299">SupportOrdering</span></span>

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="a4e68-300">**TopicAttribute 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="a4e68-301">다음 속성은 사용되지 않음으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="a4e68-302">위치</span><span class="sxs-lookup"><span data-stu-id="a4e68-302">Location</span></span>
    - <span data-ttu-id="a4e68-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="a4e68-303">IsExpress</span></span>
    - <span data-ttu-id="a4e68-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="a4e68-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="a4e68-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="a4e68-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="a4e68-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="a4e68-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="a4e68-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="a4e68-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="a4e68-308">**SubscriptionAttribute 형식**</span><span class="sxs-lookup"><span data-stu-id="a4e68-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="a4e68-309">다음 속성은 사용되지 않음으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e68-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="a4e68-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="a4e68-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="a4e68-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="a4e68-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="a4e68-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="a4e68-312">IsReadOnly</span></span>
    - <span data-ttu-id="a4e68-313">위치</span><span class="sxs-lookup"><span data-stu-id="a4e68-313">Location</span></span>
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```