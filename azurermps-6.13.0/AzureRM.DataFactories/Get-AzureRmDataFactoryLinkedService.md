---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 8a6553547bd75aeaaca8e96a85c9697d00ee65a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536675"
---
# <span data-ttu-id="287c6-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="287c6-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="287c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287c6-102">SYNOPSIS</span></span>
<span data-ttu-id="287c6-103">Azure Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="287c6-104">SYNTAX</span></span>

### <span data-ttu-id="287c6-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="287c6-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="287c6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="287c6-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="287c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="287c6-107">DESCRIPTION</span></span>
<span data-ttu-id="287c6-108">**AzureRmDataFactoryLinkedService** Cmdlet은 Azure Data Factory의 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="287c6-109">연결 된 서비스의 이름을 지정 하는 경우이 cmdlet은 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="287c6-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="287c6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="287c6-111">EXAMPLES</span></span>

### <span data-ttu-id="287c6-112">예제 1: 연결 된 모든 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="287c6-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="287c6-113">이 명령은 WikiADF 이라는 데이터 팩터리에 연결 된 모든 서비스에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 연결 된 서비스를 Format-List cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="287c6-114">해당 cmdlet은 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="287c6-115">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="287c6-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="287c6-116">예제 2: 연결 된 특정 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="287c6-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="287c6-117">이 명령은 WikiADF 이라는 data factory에서 HDILinkedService 라는 연결 된 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="287c6-118">예제 3: DataFactory 매개 변수를 지정 하 여 특정 연결 된 서비스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="287c6-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="287c6-119">첫 번째 명령은 Get-AzureRmDataFactory cmdlet을 사용 하 여 ContosoFactory 이라는 data factory를 가져오고이를 $DataFactory 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="287c6-120">두 번째 명령은 $DataFactory에 저장 된 data factory에 대 한 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 해당 정보를 Format-Table cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="287c6-121">**Format-테이블** 출력의 형식을 데이터 집합 열로 지정 된 속성을 갖는 데이터 집합으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="287c6-122">변수</span><span class="sxs-lookup"><span data-stu-id="287c6-122">PARAMETERS</span></span>

### <span data-ttu-id="287c6-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="287c6-123">-DataFactory</span></span>
<span data-ttu-id="287c6-124">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="287c6-125">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="287c6-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="287c6-126">-DataFactoryName</span></span>
<span data-ttu-id="287c6-127">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="287c6-128">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="287c6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287c6-129">-DefaultProfile</span></span>
<span data-ttu-id="287c6-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="287c6-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="287c6-131">-이름</span><span class="sxs-lookup"><span data-stu-id="287c6-131">-Name</span></span>
<span data-ttu-id="287c6-132">정보를 가져올 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-132">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287c6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287c6-133">-ResourceGroupName</span></span>
<span data-ttu-id="287c6-134">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="287c6-135">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 연결 된 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="287c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287c6-136">CommonParameters</span></span>
<span data-ttu-id="287c6-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="287c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287c6-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287c6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287c6-139">입력</span><span class="sxs-lookup"><span data-stu-id="287c6-139">INPUTS</span></span>

### <span data-ttu-id="287c6-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="287c6-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="287c6-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="287c6-141">System.String</span></span>

## <span data-ttu-id="287c6-142">출력</span><span class="sxs-lookup"><span data-stu-id="287c6-142">OUTPUTS</span></span>

### <span data-ttu-id="287c6-143">DataFactories. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="287c6-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="287c6-144">상속자</span><span class="sxs-lookup"><span data-stu-id="287c6-144">NOTES</span></span>
* <span data-ttu-id="287c6-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="287c6-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="287c6-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="287c6-146">RELATED LINKS</span></span>

[<span data-ttu-id="287c6-147">새로운 AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="287c6-147">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="287c6-148">제거-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="287c6-148">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)

