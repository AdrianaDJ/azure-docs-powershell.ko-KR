---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: d25e9aeb75c58bcce560043d87f5ce9eef065b97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532508"
---
# <span data-ttu-id="c3677-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c3677-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="c3677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3677-102">SYNOPSIS</span></span>
<span data-ttu-id="c3677-103">계산 노드에 대 한 원격 로그온 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3677-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3677-104">SYNTAX</span></span>

### <span data-ttu-id="c3677-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="c3677-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3677-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c3677-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3677-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c3677-107">DESCRIPTION</span></span>
<span data-ttu-id="c3677-108">**AzureBatchRemoteLoginSettings** cmdlet은 가상 컴퓨터 인프라 기반 풀의 계산 노드에 대 한 원격 로그온 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="c3677-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c3677-109">EXAMPLES</span></span>

### <span data-ttu-id="c3677-110">예제 1: 풀의 모든 노드에 대 한 원격 로그온 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3677-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="c3677-111">첫 번째 명령은 **AzureRmBatchAccountKeys** 를 사용 하 여 구독에 대 한 선택 키를 포함 하는 일괄 처리 계정 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="c3677-112">명령은 다음 명령에 사용할 컨텍스트를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="c3677-113">두 번째 명령은 **Get-AzureBatchComputeNode** 를 사용 하 여 ID ContosoPool를 가진 풀의 각 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="c3677-114">이 명령은 파이프라인 연산자를 사용 하 여 각 컴퓨터 노드를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3677-115">명령은 각 계산 노드에 대 한 원격 로그온 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="c3677-116">예제 2: 노드에 대 한 원격 로그온 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3677-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="c3677-117">첫 번째 명령은 구독에 대 한 선택 키를 포함 하는 일괄 처리 계정 컨텍스트를 가져온 다음 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="c3677-118">두 번째 명령은 ID ContosoPool를 가진 풀에서 지정 된 ID를 갖는 계산 노드에 대 한 원격 로그온 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="c3677-119">변수</span><span class="sxs-lookup"><span data-stu-id="c3677-119">PARAMETERS</span></span>

### <span data-ttu-id="c3677-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3677-120">-BatchContext</span></span>
<span data-ttu-id="c3677-121">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3677-122">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3677-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3677-123">-ComputeNode</span></span>
<span data-ttu-id="c3677-124">이 cmdlet에서 원격 로그온 설정을 가져오는 계산 노드를 **PSComputeNode** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="c3677-125">계산 노드 개체를 가져오려면 Get-AzureBatchComputeNode cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3677-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c3677-126">-ComputeNodeId</span></span>
<span data-ttu-id="c3677-127">원격 로그온 설정을 가져올 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="c3677-128">이 cmdlet에 대 한 원격 로그온 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3677-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3677-129">-DefaultProfile</span></span>
<span data-ttu-id="c3677-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3677-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c3677-131">-PoolId</span></span>
<span data-ttu-id="c3677-132">가상 컴퓨터를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3677-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3677-133">CommonParameters</span></span>
<span data-ttu-id="c3677-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3677-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3677-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3677-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3677-136">입력</span><span class="sxs-lookup"><span data-stu-id="c3677-136">INPUTS</span></span>

### <span data-ttu-id="c3677-137">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3677-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="c3677-138">매개 변수: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3677-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="c3677-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3677-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c3677-140">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3677-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c3677-141">출력</span><span class="sxs-lookup"><span data-stu-id="c3677-141">OUTPUTS</span></span>

### <span data-ttu-id="c3677-142">Microsoft.Azure.Commands.Batch. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c3677-142">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="c3677-143">상속자</span><span class="sxs-lookup"><span data-stu-id="c3677-143">NOTES</span></span>

## <span data-ttu-id="c3677-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3677-144">RELATED LINKS</span></span>

[<span data-ttu-id="c3677-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c3677-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c3677-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3677-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="c3677-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="c3677-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="c3677-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c3677-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

