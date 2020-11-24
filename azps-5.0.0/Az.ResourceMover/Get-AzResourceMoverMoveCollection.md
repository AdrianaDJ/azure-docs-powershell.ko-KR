---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309958"
---
# <span data-ttu-id="c9585-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c9585-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="c9585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9585-102">SYNOPSIS</span></span>
<span data-ttu-id="c9585-103">이동 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-103">Gets the move collection.</span></span>

## <span data-ttu-id="c9585-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9585-104">SYNTAX</span></span>

### <span data-ttu-id="c9585-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c9585-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9585-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="c9585-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9585-107">List1</span><span class="sxs-lookup"><span data-stu-id="c9585-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9585-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c9585-108">DESCRIPTION</span></span>
<span data-ttu-id="c9585-109">이동 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-109">Gets the move collection.</span></span>

## <span data-ttu-id="c9585-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c9585-110">EXAMPLES</span></span>

### <span data-ttu-id="c9585-111">예제 1: 구독의 모든 이동 컬렉션에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9585-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="c9585-112">구독의 모든 이동 컬렉션에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="c9585-113">예제 2: 구독에서 지정 된 move collection 이름으로 이동 컬렉션의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9585-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="c9585-114">구독에서 지정 된 move collection 이름으로 이동 컬렉션에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="c9585-115">예제 3: 구독에서 지정 된 리소스 그룹 이름을 갖는 Move collection에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9585-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="c9585-116">구독에서 지정 된 리소스 그룹 이름을 갖는 Move Collection에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="c9585-117">변수</span><span class="sxs-lookup"><span data-stu-id="c9585-117">PARAMETERS</span></span>

### <span data-ttu-id="c9585-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9585-118">-DefaultProfile</span></span>
<span data-ttu-id="c9585-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9585-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c9585-120">-Name</span></span>
<span data-ttu-id="c9585-121">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9585-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9585-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9585-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9585-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9585-124">-SubscriptionId</span></span>
<span data-ttu-id="c9585-125">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-125">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9585-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9585-126">CommonParameters</span></span>
<span data-ttu-id="c9585-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9585-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9585-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9585-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9585-129">입력</span><span class="sxs-lookup"><span data-stu-id="c9585-129">INPUTS</span></span>

## <span data-ttu-id="c9585-130">출력</span><span class="sxs-lookup"><span data-stu-id="c9585-130">OUTPUTS</span></span>

### <span data-ttu-id="c9585-131">Api20191001Preview를 통해. a. i. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9585-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="c9585-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c9585-132">NOTES</span></span>

<span data-ttu-id="c9585-133">별칭과</span><span class="sxs-lookup"><span data-stu-id="c9585-133">ALIASES</span></span>

## <span data-ttu-id="c9585-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9585-134">RELATED LINKS</span></span>
