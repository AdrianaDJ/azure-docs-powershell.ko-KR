---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309926"
---
# <span data-ttu-id="60cc5-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="60cc5-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="60cc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="60cc5-103">요청 본문에 포함 된 리소스 집합에 대 한 준비를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="60cc5-104">준비 작업은 moveState ' PreparePending ' 또는 ' PrepareFailed ' 인 moveResources에 있으며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="60cc5-105">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="60cc5-106">구문과</span><span class="sxs-lookup"><span data-stu-id="60cc5-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60cc5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="60cc5-107">DESCRIPTION</span></span>
<span data-ttu-id="60cc5-108">요청 본문에 포함 된 리소스 집합에 대 한 준비를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="60cc5-109">준비 작업은 moveState ' PreparePending ' 또는 ' PrepareFailed ' 인 moveResources에 있으며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="60cc5-110">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="60cc5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="60cc5-111">EXAMPLES</span></span>

### <span data-ttu-id="60cc5-112">예제 1: 리소스를 준비 하기 전에 dependecies의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="60cc5-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="60cc5-113">리소스를 준비 하기 전에 dependecies의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="60cc5-114">예제 2: "MoveResource Name"을 입력으로 사용 하는 Move Collection에서 리소스 집합에 대 한 준비 시작</span><span class="sxs-lookup"><span data-stu-id="60cc5-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="60cc5-115">"MoveResource Name"을 입력으로 사용 하 여 Move Collection의 리소스 집합에 대 한 준비를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="60cc5-116">예제 3: "Sourc? Mid"를 사용 하 여 Move Collection의 리소스 집합에 대 한 준비 시작</span><span class="sxs-lookup"><span data-stu-id="60cc5-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="60cc5-117">"Sourc? Mid"를 사용 하 여 Move Collection의 리소스 집합에 대 한 준비를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="60cc5-118">변수</span><span class="sxs-lookup"><span data-stu-id="60cc5-118">PARAMETERS</span></span>

### <span data-ttu-id="60cc5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60cc5-119">-AsJob</span></span>
<span data-ttu-id="60cc5-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="60cc5-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cc5-121">-DefaultProfile</span></span>
<span data-ttu-id="60cc5-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="60cc5-123">-MoveCollectionName</span></span>
<span data-ttu-id="60cc5-124">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-124">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="60cc5-125">-MoveResource</span></span>
<span data-ttu-id="60cc5-126">리소스 Id의 목록을 가져오거나 설정 합니다. 기본적으로 입력 형식이 moveResourceInputType 속성을 통해 전환 되지 않는 한 리소스 id 이동을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="60cc5-127">-MoveResourceInputType</span></span>
<span data-ttu-id="60cc5-128">리소스 이동 입력 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="60cc5-129">-NoWait</span></span>
<span data-ttu-id="60cc5-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="60cc5-130">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cc5-131">-ResourceGroupName</span></span>
<span data-ttu-id="60cc5-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-132">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60cc5-133">-SubscriptionId</span></span>
<span data-ttu-id="60cc5-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-134">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="60cc5-135">-ValidateOnly</span></span>
<span data-ttu-id="60cc5-136">작업에서 필수 요소를 사전에만 실행 해야 하는지 여부를 나타내는 값을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-137">-확인</span><span class="sxs-lookup"><span data-stu-id="60cc5-137">-Confirm</span></span>
<span data-ttu-id="60cc5-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60cc5-139">-WhatIf</span></span>
<span data-ttu-id="60cc5-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60cc5-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cc5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cc5-142">CommonParameters</span></span>
<span data-ttu-id="60cc5-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cc5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cc5-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60cc5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cc5-145">입력</span><span class="sxs-lookup"><span data-stu-id="60cc5-145">INPUTS</span></span>

## <span data-ttu-id="60cc5-146">출력</span><span class="sxs-lookup"><span data-stu-id="60cc5-146">OUTPUTS</span></span>

### <span data-ttu-id="60cc5-147">Api20191001Preview를 통해. PowerShell. a. i. i a m-IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="60cc5-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="60cc5-148">상속자</span><span class="sxs-lookup"><span data-stu-id="60cc5-148">NOTES</span></span>

<span data-ttu-id="60cc5-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="60cc5-149">ALIASES</span></span>

## <span data-ttu-id="60cc5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60cc5-150">RELATED LINKS</span></span>
