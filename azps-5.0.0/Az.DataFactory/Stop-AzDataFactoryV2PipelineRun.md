---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305942"
---
# <span data-ttu-id="f010e-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f010e-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="f010e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f010e-102">SYNOPSIS</span></span>
<span data-ttu-id="f010e-103">데이터 팩터리에 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="f010e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f010e-104">SYNTAX</span></span>

### <span data-ttu-id="f010e-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f010e-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f010e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f010e-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f010e-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f010e-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f010e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f010e-108">DESCRIPTION</span></span>
<span data-ttu-id="f010e-109">**AzDataFactoryV2PipelineRun** cmdlet은 파이프라인 실행 ID를 사용 하 여 지정 된 데이터 팩터리에 파이프라인을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="f010e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f010e-110">EXAMPLES</span></span>

### <span data-ttu-id="f010e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f010e-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="f010e-112">이 명령은 factory WikiADF에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd의 파이프라인 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="f010e-113">변수</span><span class="sxs-lookup"><span data-stu-id="f010e-113">PARAMETERS</span></span>

### <span data-ttu-id="f010e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f010e-114">-DataFactory</span></span>
<span data-ttu-id="f010e-115">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f010e-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f010e-116">-DataFactoryName</span></span>
<span data-ttu-id="f010e-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f010e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f010e-118">-DefaultProfile</span></span>
<span data-ttu-id="f010e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f010e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f010e-120">-InputObject</span></span>
<span data-ttu-id="f010e-121">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f010e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f010e-122">-PassThru</span></span>
<span data-ttu-id="f010e-123">지정 된 경우 cmdlet 쓰기 true를 대/소문자 구분 작업에 성공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="f010e-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="f010e-124">-PipelineRunId</span></span>
<span data-ttu-id="f010e-125">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f010e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f010e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f010e-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f010e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="f010e-128">-Confirm</span></span>
<span data-ttu-id="f010e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f010e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f010e-130">-WhatIf</span></span>
<span data-ttu-id="f010e-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f010e-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f010e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f010e-133">CommonParameters</span></span>
<span data-ttu-id="f010e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f010e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f010e-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f010e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f010e-136">입력</span><span class="sxs-lookup"><span data-stu-id="f010e-136">INPUTS</span></span>

### <span data-ttu-id="f010e-137">DataFactoryV2. PSPipelineRun/.</span><span class="sxs-lookup"><span data-stu-id="f010e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="f010e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f010e-138">System.String</span></span>

### <span data-ttu-id="f010e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f010e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f010e-140">출력</span><span class="sxs-lookup"><span data-stu-id="f010e-140">OUTPUTS</span></span>

### <span data-ttu-id="f010e-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f010e-141">System.Boolean</span></span>

## <span data-ttu-id="f010e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f010e-142">NOTES</span></span>

## <span data-ttu-id="f010e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f010e-143">RELATED LINKS</span></span>