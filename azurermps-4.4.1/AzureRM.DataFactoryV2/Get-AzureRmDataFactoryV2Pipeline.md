---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537328"
---
# <span data-ttu-id="0d998-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0d998-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="0d998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d998-102">SYNOPSIS</span></span>
<span data-ttu-id="0d998-103">Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d998-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d998-104">SYNTAX</span></span>

### <span data-ttu-id="0d998-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d998-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="0d998-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0d998-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="0d998-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0d998-107">DESCRIPTION</span></span>
<span data-ttu-id="0d998-108">Get-AzureRmDataFactoryV2Pipeline cmdlet은 Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="0d998-109">파이프라인의 이름을 지정 하는 경우이 cmdlet은 해당 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="0d998-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="0d998-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0d998-111">EXAMPLES</span></span>

### <span data-ttu-id="0d998-112">예제 1: 모든 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d998-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="0d998-113">이 명령은 WikiADF 이라는 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="0d998-114">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="0d998-115">두 번째는 DataFactory 개체를 매개 변수로 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="0d998-116">예제 2: 특정 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d998-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="0d998-117">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="0d998-118">이 명령은 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 해당 정보를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d998-119">해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0d998-120">자세한 내용을 보려면 Get-Help 서식 목록을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="0d998-121">예제 3: 특정 파이프라인의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d998-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

<span data-ttu-id="0d998-122">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 작업 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="0d998-123">예제 6: 첫 번째 활동의 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d998-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

<span data-ttu-id="0d998-124">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 작업 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="0d998-125">이 명령은 Format-List cmdlet을 사용 하 여 활동 배열의 첫 번째 요소의 입력 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="0d998-126">변수</span><span class="sxs-lookup"><span data-stu-id="0d998-126">PARAMETERS</span></span>

### <span data-ttu-id="0d998-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0d998-127">-DataFactory</span></span>
<span data-ttu-id="0d998-128">PSDataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="0d998-129">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d998-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0d998-130">-DataFactoryName</span></span>
<span data-ttu-id="0d998-131">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0d998-132">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d998-133">-이름</span><span class="sxs-lookup"><span data-stu-id="0d998-133">-Name</span></span>
<span data-ttu-id="0d998-134">정보를 가져올 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d998-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d998-135">-ResourceGroupName</span></span>
<span data-ttu-id="0d998-136">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0d998-137">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="0d998-138">입력</span><span class="sxs-lookup"><span data-stu-id="0d998-138">INPUTS</span></span>

### <span data-ttu-id="0d998-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d998-139">System.String</span></span>
<span data-ttu-id="0d998-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0d998-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="0d998-141">출력</span><span class="sxs-lookup"><span data-stu-id="0d998-141">OUTPUTS</span></span>

### <span data-ttu-id="0d998-142">DataFactoryV2 ' 1 [[Microsoft Azure. PSPipeline, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0d998-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0d998-143">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="0d998-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="0d998-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0d998-144">NOTES</span></span>
<span data-ttu-id="0d998-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="0d998-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0d998-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d998-146">RELATED LINKS</span></span>
[<span data-ttu-id="0d998-147">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0d998-147">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0d998-148">제거-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0d998-148">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0d998-149">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="0d998-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()