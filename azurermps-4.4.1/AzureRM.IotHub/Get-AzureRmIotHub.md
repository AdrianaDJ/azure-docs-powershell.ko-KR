---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537156"
---
# <span data-ttu-id="d39fe-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="d39fe-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="d39fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d39fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d39fe-103">구독에서 IotHubs에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d39fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d39fe-104">SYNTAX</span></span>

### <span data-ttu-id="d39fe-105">ListIotHubsByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="d39fe-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d39fe-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="d39fe-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d39fe-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d39fe-107">DESCRIPTION</span></span>
<span data-ttu-id="d39fe-108">구독에서 IotHubs에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="d39fe-109">구독에서 모든 IotHub 인스턴스를 보거나 리소스 그룹 또는 특정 IotHub 이름을 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="d39fe-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d39fe-110">EXAMPLES</span></span>

### <span data-ttu-id="d39fe-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d39fe-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="d39fe-112">구독에 있는 모든 IotHubs를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="d39fe-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d39fe-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="d39fe-114">"Myresourcegroup" 이라는 리소스 이름에 속하는 구독의 모든 IotHubs를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="d39fe-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d39fe-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d39fe-116">이름이 "myiothub" 인 IotHub에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="d39fe-117">변수</span><span class="sxs-lookup"><span data-stu-id="d39fe-117">PARAMETERS</span></span>

### <span data-ttu-id="d39fe-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d39fe-118">-Name</span></span>
<span data-ttu-id="d39fe-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="d39fe-121">ResourceGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-121">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39fe-122">-DefaultProfile</span></span>
<span data-ttu-id="d39fe-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d39fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39fe-124">CommonParameters</span></span>
<span data-ttu-id="d39fe-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d39fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39fe-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39fe-127">입력</span><span class="sxs-lookup"><span data-stu-id="d39fe-127">INPUTS</span></span>

### <span data-ttu-id="d39fe-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d39fe-128">System.String</span></span>

## <span data-ttu-id="d39fe-129">출력</span><span class="sxs-lookup"><span data-stu-id="d39fe-129">OUTPUTS</span></span>

### <span data-ttu-id="d39fe-130">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="d39fe-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="d39fe-131">\` \[ \[ PSIotHub, IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = Null 인 경우 목록 1에 있는. a. i a.\]\]</span><span class="sxs-lookup"><span data-stu-id="d39fe-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="d39fe-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d39fe-132">NOTES</span></span>

## <span data-ttu-id="d39fe-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d39fe-133">RELATED LINKS</span></span>
