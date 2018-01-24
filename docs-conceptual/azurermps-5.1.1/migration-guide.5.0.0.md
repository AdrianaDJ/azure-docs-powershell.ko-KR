# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="b52fc-101">Microsoft Azure PowerShell 5.0.0의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="b52fc-102">이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b52fc-103">각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="b52fc-104">심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="b52fc-105">목차</span><span class="sxs-lookup"><span data-stu-id="b52fc-105">Table of Contents</span></span>

- [<span data-ttu-id="b52fc-106">ApiManagement cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="b52fc-107">Batch cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="b52fc-108">Compute cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="b52fc-109">EventHub cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="b52fc-110">Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="b52fc-111">Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="b52fc-112">Resources cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="b52fc-113">ServiceBus cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="b52fc-114">ApiManagement cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="b52fc-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="b52fc-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="b52fc-116">매개 변수 "UserName" 및 "Password"가 PSCredential에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="b52fc-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="b52fc-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="b52fc-118">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="b52fc-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="b52fc-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="b52fc-120">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="b52fc-121">Batch cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="b52fc-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="b52fc-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="b52fc-123">매개 변수 `Password`가 보안 문자열에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="b52fc-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="b52fc-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="b52fc-125">매개 변수 `Password`가 보안 문자열에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="b52fc-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="b52fc-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="b52fc-127">매개 변수 `Password`가 보안 문자열에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="b52fc-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="b52fc-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="b52fc-129">`RunElevated` 스위치가 제거되고 `UserIdentity`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="b52fc-130">또한 `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` 및 `PSJobReleaseTask`의 `RunElevated` 속성에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="b52fc-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="b52fc-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="b52fc-132">`PSMultiInstanceSettings` 생성자는 더 이상 필수 `numberOfInstances` 매개 변수를 사용하지 않고 대신 필수 `coordinationCommandLine` 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="b52fc-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="b52fc-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="b52fc-134">`PSCloudTask`에서 `RunElevated` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="b52fc-135">`UserIdentity`를 대체하기 위해 `RunElevated` 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="b52fc-136">또한 `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` 및 `PSJobReleaseTask`의 `RunElevated` 속성에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="b52fc-137">**여러 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-137">**Multiple types**</span></span>

- <span data-ttu-id="b52fc-138">`PSExitConditions`에서 `SchedulingError` 속성의 이름이 `PreProcessingError`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="b52fc-139">**여러 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-139">**Multiple types**</span></span>

- <span data-ttu-id="b52fc-140">`PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` 및 `PSTaskExecutionInformation`에서 `SchedulingError` 속성의 이름이 `FailureInformation`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="b52fc-141">작업 실패가 있을 때마다 `FailureInformation`이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="b52fc-142">여기에는 이전의 모든 예약 오류 사례는 물론, 0이 아닌 작업 종료 코드 및 새 출력 파일 기능의 파일 업로드 오류가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="b52fc-143">이것은 이전과 동일하게 구성되므로 이 형식을 사용할 때는 코드 변경 내용이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="b52fc-144">또한 Get-AzureBatchPool, Get-AzureBatchSubtask 및 Get-AzureBatchJobPreparationAndReleaseTaskStatus에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="b52fc-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="b52fc-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="b52fc-146">`TargetDedicated`가 제거되고 `TargetDedicatedComputeNodes` 및 `TargetLowPriorityComputeNodes`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="b52fc-147">`TargetDedicatedComputeNodes`에 `TargetDedicated` 별칭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="b52fc-148">또한 Start-AzureBatchPoolResize에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="b52fc-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="b52fc-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="b52fc-150">`PSCloudPool`에서 `TargetDedicated` 및 `CurrentDedicated` 속성 이름이 `TargetDedicatedComputeNodes` 및 `CurrentDedicatedComputeNodes`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="b52fc-151">**PSCloudPool 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="b52fc-152">`PSCloudPool`에서 `ResizeError`의 이름이 `ResizeErrors`로 변경되었고 이제 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="b52fc-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="b52fc-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="b52fc-154">`PSPoolSpecification`에서 `TargetDedicated` 속성의 이름이 `TargetDedicatedComputeNodes`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="b52fc-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="b52fc-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="b52fc-156">`Name`이 제거되고 `Path`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="b52fc-157">`Path`에 `Name` 별칭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="b52fc-158">또한 Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile에도 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="b52fc-159">**PSNodeFile** 형식</span><span class="sxs-lookup"><span data-stu-id="b52fc-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="b52fc-160">`PSNodeFile`에서 `Name` 속성의 이름이 `Path`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="b52fc-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="b52fc-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="b52fc-162">`PSSubtaskInformation`의 `PreviousState` 및 `State` 속성은 더 이상 `TaskState` 형식이 아니며, 대신 `SubtaskState` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="b52fc-163">하위 작업이 `Active` 상태가 될 수 없으므로, `TaskState`와 달리, `SubtaskState`에는 `Active` 값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="b52fc-164">Compute cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="b52fc-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="b52fc-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="b52fc-166">매개 변수 "UserName" 및 "Password"가 PSCredential에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="b52fc-167">EventHub cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-169">'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-170">'New-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-172">'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-173">'Get-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-175">'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-176">'Set-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-178">'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-179">'Remove-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="b52fc-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="b52fc-181">'New-AzureRmEventHubNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-182">'New-AzureRmEventHubKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="b52fc-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="b52fc-184">'Get-AzureRmEventHubNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-185">'Get-AzureRmEventHubKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="b52fc-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="b52fc-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="b52fc-187">NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="b52fc-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="b52fc-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="b52fc-189">NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="b52fc-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="b52fc-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="b52fc-191">NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="b52fc-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="b52fc-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="b52fc-193">ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="b52fc-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="b52fc-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="b52fc-195">ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="b52fc-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="b52fc-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="b52fc-197">ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="b52fc-198">Insights cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="b52fc-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="b52fc-200">**Add-AzureRMLogAlertRule** cmdlet이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="b52fc-201">이 cmdlet을 사용하는 10월 1일 이후에는 이 기능이 활동 로그 경고로 전환되므로 더 이상 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="b52fc-202">자세한 내용은 https://aka.ms/migratemealerts를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="b52fc-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="b52fc-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="b52fc-204">**Get-AzureRMUsage** cmdlet이 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="b52fc-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="b52fc-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="b52fc-206">출력 변경: 이제 상수 값(Admin,Operation)을 반환하므로 EventData 개체(이러한 cmdlet에서 반환됨)의 EventChannels 필드가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="b52fc-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="b52fc-208">출력 변경: 이 cmdlet의 출력은 속성 필드를 제거하도록 평면화되어 사용자 환경을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="b52fc-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="b52fc-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="b52fc-210">출력 변경: AutoscaleSettingResourceName 필드는 항상 이름 필드와 같으므로 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="b52fc-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="b52fc-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="b52fc-212">출력 변경: 출력 형식은 요청 ID 및 상태 코드가 포함된 단일 개체를 반환하도록 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="b52fc-213">Network cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="b52fc-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="b52fc-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="b52fc-215">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="b52fc-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="b52fc-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="b52fc-217">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="b52fc-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="b52fc-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="b52fc-219">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="b52fc-220">Resources cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="b52fc-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="b52fc-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="b52fc-222">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="b52fc-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="b52fc-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="b52fc-224">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="b52fc-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="b52fc-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="b52fc-226">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="b52fc-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="b52fc-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="b52fc-228">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="b52fc-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="b52fc-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="b52fc-230">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="b52fc-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="b52fc-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="b52fc-232">매개 변수 "Password"가 SecureString에 대해 대체됨</span><span class="sxs-lookup"><span data-stu-id="b52fc-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="b52fc-233">ServiceBus cmdlet의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b52fc-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="b52fc-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-235">'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-236">'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="b52fc-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="b52fc-238">'Get-AzureRmServiceBusTopicKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-239">'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="b52fc-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-241">'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-242">'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="b52fc-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="b52fc-244">'New-AzureRmServiceBusTopicKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-245">'New-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="b52fc-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-247">'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-248">'Remove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="b52fc-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-250">'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-251">'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="b52fc-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="b52fc-253">'New-AzureRmServiceBusNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-254">'New-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="b52fc-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-256">'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-257">'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="b52fc-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="b52fc-259">'Get-AzureRmServiceBusQueueKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-260">'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="b52fc-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-262">'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-263">'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="b52fc-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="b52fc-265">'New-AzureRmServiceBusQueueKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-266">'New-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="b52fc-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-268">'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-269">'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="b52fc-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-271">'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-272">'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-274">'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-275">'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="b52fc-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="b52fc-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="b52fc-277">'Get-AzureRmServiceBusNamespaceKey' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-278">'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-280">'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-281">'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-283">'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-284">'Remove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="b52fc-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="b52fc-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="b52fc-286">'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="b52fc-287">'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="b52fc-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="b52fc-288">**NamespaceAttributes 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="b52fc-289">다음 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-289">The following properties have been removed</span></span>
    - <span data-ttu-id="b52fc-290">사용</span><span class="sxs-lookup"><span data-stu-id="b52fc-290">Enabled</span></span>
    - <span data-ttu-id="b52fc-291">상태</span><span class="sxs-lookup"><span data-stu-id="b52fc-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="b52fc-292">**QueueAttribute 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="b52fc-293">다음 속성은 사용되지 않음으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="b52fc-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b52fc-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="b52fc-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="b52fc-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="b52fc-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="b52fc-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="b52fc-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="b52fc-297">SupportOrdering</span></span>

```powershell
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
   
### <a name="type-topicattribute"></a><span data-ttu-id="b52fc-298">**TopicAttribute 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="b52fc-299">다음 속성은 사용되지 않음으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="b52fc-300">위치</span><span class="sxs-lookup"><span data-stu-id="b52fc-300">Location</span></span>
    - <span data-ttu-id="b52fc-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="b52fc-301">IsExpress</span></span>
    - <span data-ttu-id="b52fc-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="b52fc-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="b52fc-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="b52fc-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="b52fc-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="b52fc-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="b52fc-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="b52fc-305">EntityAvailabilityStatus</span></span>

```powershell
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
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="b52fc-306">**SubscriptionAttribute 형식**</span><span class="sxs-lookup"><span data-stu-id="b52fc-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="b52fc-307">다음 속성은 사용되지 않음으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b52fc-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="b52fc-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="b52fc-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="b52fc-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="b52fc-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="b52fc-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="b52fc-310">IsReadOnly</span></span>
    - <span data-ttu-id="b52fc-311">위치</span><span class="sxs-lookup"><span data-stu-id="b52fc-311">Location</span></span>
   
```powershell
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