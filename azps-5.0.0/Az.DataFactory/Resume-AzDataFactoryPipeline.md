---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 237e91df7826e1d524e352e9d2502b7edac8c271
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306050"
---
# <span data-ttu-id="06168-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="06168-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="06168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06168-102">SYNOPSIS</span></span>
<span data-ttu-id="06168-103">Data Factory에서 일시 중단 된 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="06168-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06168-104">SYNTAX</span></span>

### <span data-ttu-id="06168-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="06168-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06168-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="06168-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06168-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06168-107">DESCRIPTION</span></span>
<span data-ttu-id="06168-108">**AzDataFactoryPipeline** Cmdlet은 Azure Data Factory에서 일시 중단 된 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="06168-109">예제의</span><span class="sxs-lookup"><span data-stu-id="06168-109">EXAMPLES</span></span>

### <span data-ttu-id="06168-110">예제 1: 파이프라인 다시 시작</span><span class="sxs-lookup"><span data-stu-id="06168-110">Example 1: Resume a pipeline</span></span>
```powershell
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="06168-111">이 명령은 WikiADF 이라는 data factory에서 DPWikisample 라는 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="06168-112">파이프라인을 일시 중단 하려면 **AzDataFactoryPipeline** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="06168-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-113">The command returns a value of $True.</span></span>

### <span data-ttu-id="06168-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="06168-114">Example 2</span></span>

<span data-ttu-id="06168-115">Data Factory에서 일시 중단 된 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-115">Resumes a suspended pipeline in Data Factory.</span></span> <span data-ttu-id="06168-116">생성</span><span class="sxs-lookup"><span data-stu-id="06168-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Resume-AzDataFactoryPipeline -DataFactory $DataFactory -Name 'DPWikisample'
```

## <span data-ttu-id="06168-117">변수</span><span class="sxs-lookup"><span data-stu-id="06168-117">PARAMETERS</span></span>

### <span data-ttu-id="06168-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="06168-118">-DataFactory</span></span>
<span data-ttu-id="06168-119">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="06168-120">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06168-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="06168-121">-DataFactoryName</span></span>
<span data-ttu-id="06168-122">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="06168-123">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-123">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="06168-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06168-124">-DefaultProfile</span></span>
<span data-ttu-id="06168-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06168-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06168-126">-이름</span><span class="sxs-lookup"><span data-stu-id="06168-126">-Name</span></span>
<span data-ttu-id="06168-127">다시 시작할 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-127">Specifies the name of the pipeline to resume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06168-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06168-128">-ResourceGroupName</span></span>
<span data-ttu-id="06168-129">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="06168-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-130">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="06168-131">-확인</span><span class="sxs-lookup"><span data-stu-id="06168-131">-Confirm</span></span>
<span data-ttu-id="06168-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06168-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06168-133">-WhatIf</span></span>
<span data-ttu-id="06168-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06168-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06168-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06168-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06168-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06168-136">CommonParameters</span></span>
<span data-ttu-id="06168-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06168-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06168-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06168-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06168-139">입력</span><span class="sxs-lookup"><span data-stu-id="06168-139">INPUTS</span></span>

### <span data-ttu-id="06168-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06168-140">System.String</span></span>

### <span data-ttu-id="06168-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="06168-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="06168-142">출력</span><span class="sxs-lookup"><span data-stu-id="06168-142">OUTPUTS</span></span>

### <span data-ttu-id="06168-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="06168-143">System.Boolean</span></span>

## <span data-ttu-id="06168-144">상속자</span><span class="sxs-lookup"><span data-stu-id="06168-144">NOTES</span></span>
* <span data-ttu-id="06168-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="06168-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="06168-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06168-146">RELATED LINKS</span></span>

[<span data-ttu-id="06168-147">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="06168-147">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="06168-148">새로운 AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="06168-148">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="06168-149">제거-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="06168-149">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="06168-150">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="06168-150">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="06168-151">일시 중단-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="06168-151">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

