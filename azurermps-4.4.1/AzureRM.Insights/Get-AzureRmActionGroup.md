---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 4edb403452d262705fe8fa61691ac77ba4524977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537172"
---
# <span data-ttu-id="bac72-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="bac72-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="bac72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac72-102">SYNOPSIS</span></span>
<span data-ttu-id="bac72-103">작업 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bac72-104">SYNTAX</span></span>

### <span data-ttu-id="bac72-105">BySubscriptionOrResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="bac72-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bac72-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bac72-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bac72-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bac72-107">DESCRIPTION</span></span>
<span data-ttu-id="bac72-108">**Get-AzureRmActionGroup** cmdlet은 하나 이상의 작업 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="bac72-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bac72-109">EXAMPLES</span></span>

### <span data-ttu-id="bac72-110">예제 1: 구독 ID를 기준으로 작업 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="bac72-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="bac72-111">이 명령은 현재 구독에 대 한 모든 작업 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="bac72-112">예제 2: 지정 된 리소스 그룹에 대 한 작업 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="bac72-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="bac72-113">이 명령은 지정 된 리소스 그룹에 대 한 작업 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="bac72-114">예제 3: 작업 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="bac72-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="bac72-115">이 명령은 하나 (단일 요소를 포함 하는 목록) 작업 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="bac72-116">변수</span><span class="sxs-lookup"><span data-stu-id="bac72-116">PARAMETERS</span></span>

### <span data-ttu-id="bac72-117">-이름</span><span class="sxs-lookup"><span data-stu-id="bac72-117">-Name</span></span>
<span data-ttu-id="bac72-118">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac72-119">-DefaultProfile</span></span>
<span data-ttu-id="bac72-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac72-121">-ResourceGroupName</span></span>
<span data-ttu-id="bac72-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bac72-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac72-123">CommonParameters</span></span>
<span data-ttu-id="bac72-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac72-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac72-126">입력</span><span class="sxs-lookup"><span data-stu-id="bac72-126">INPUTS</span></span>

### <span data-ttu-id="bac72-127">않아야</span><span class="sxs-lookup"><span data-stu-id="bac72-127">None</span></span>

## <span data-ttu-id="bac72-128">출력</span><span class="sxs-lookup"><span data-stu-id="bac72-128">OUTPUTS</span></span>

### <span data-ttu-id="bac72-129"><. 컬렉션이 ' 1 [Microsoft Azure. e. '를 나열 합니다. Psactiongrou보도 정보 클래스.</span><span class="sxs-lookup"><span data-stu-id="bac72-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="bac72-130">않아야</span><span class="sxs-lookup"><span data-stu-id="bac72-130">None</span></span>

## <span data-ttu-id="bac72-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bac72-131">NOTES</span></span>

## <span data-ttu-id="bac72-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bac72-132">RELATED LINKS</span></span>

<span data-ttu-id="bac72-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [제거-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [새로운 AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="bac72-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>