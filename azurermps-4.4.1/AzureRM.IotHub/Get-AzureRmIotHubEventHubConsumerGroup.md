---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 84da4142bdc1b5435ca895be1995c6b48b5881fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534064"
---
# <span data-ttu-id="096f9-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="096f9-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="096f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096f9-102">SYNOPSIS</span></span>
<span data-ttu-id="096f9-103">모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="096f9-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096f9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="096f9-105">DESCRIPTION</span></span>
<span data-ttu-id="096f9-106">IotHub에서 사용 하는 다른 EventHubs에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="096f9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="096f9-107">EXAMPLES</span></span>

### <span data-ttu-id="096f9-108">예제 1 원격 분석 eventhub에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="096f9-109">Myiothub iothub에 대 한 원격 분석 eventhub의 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="096f9-110">예제 2 operationsmonitoring eventhub에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="096f9-111">Myiothub iothub에 대 한 operationsMonitoringEvents eventhub의 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="096f9-112">변수</span><span class="sxs-lookup"><span data-stu-id="096f9-112">PARAMETERS</span></span>

### <span data-ttu-id="096f9-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="096f9-113">-EventHubEndpointName</span></span>
<span data-ttu-id="096f9-114">이벤트 허브 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="096f9-115">사용할 수 있는 값 이벤트, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="096f9-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096f9-116">-이름</span><span class="sxs-lookup"><span data-stu-id="096f9-116">-Name</span></span>
<span data-ttu-id="096f9-117">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="096f9-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="096f9-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096f9-120">-DefaultProfile</span></span>
<span data-ttu-id="096f9-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096f9-122">CommonParameters</span></span>
<span data-ttu-id="096f9-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="096f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096f9-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096f9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096f9-125">입력</span><span class="sxs-lookup"><span data-stu-id="096f9-125">INPUTS</span></span>

### <span data-ttu-id="096f9-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="096f9-126">System.String</span></span>

## <span data-ttu-id="096f9-127">출력</span><span class="sxs-lookup"><span data-stu-id="096f9-127">OUTPUTS</span></span>

### <span data-ttu-id="096f9-128">System.webserver ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="096f9-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="096f9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="096f9-129">NOTES</span></span>

## <span data-ttu-id="096f9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="096f9-130">RELATED LINKS</span></span>
