---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523440"
---
# <span data-ttu-id="e21ec-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e21ec-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="e21ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e21ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e21ec-103">지정 된 사용자 구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="e21ec-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="e21ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e21ec-104">SYNTAX</span></span>

### <span data-ttu-id="e21ec-105">Set (기본값)</span><span class="sxs-lookup"><span data-stu-id="e21ec-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21ec-106">리소스</span><span class="sxs-lookup"><span data-stu-id="e21ec-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21ec-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e21ec-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e21ec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e21ec-108">DESCRIPTION</span></span>
<span data-ttu-id="e21ec-109">지정 된 사용자 구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="e21ec-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="e21ec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e21ec-110">EXAMPLES</span></span>

### <span data-ttu-id="e21ec-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e21ec-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="e21ec-112">구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="e21ec-112">Updates a subscription</span></span>

## <span data-ttu-id="e21ec-113">변수</span><span class="sxs-lookup"><span data-stu-id="e21ec-113">PARAMETERS</span></span>

### <span data-ttu-id="e21ec-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e21ec-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e21ec-115">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e21ec-116">-DisplayName</span></span>
<span data-ttu-id="e21ec-117">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e21ec-118">-ExternalReferenceId</span></span>
<span data-ttu-id="e21ec-119">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e21ec-120">-InputObject</span></span>
<span data-ttu-id="e21ec-121">. 관리자. i a m. i a..</span><span class="sxs-lookup"><span data-stu-id="e21ec-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-122">-위치</span><span class="sxs-lookup"><span data-stu-id="e21ec-122">-Location</span></span>
<span data-ttu-id="e21ec-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e21ec-124">-OfferId</span></span>
<span data-ttu-id="e21ec-125">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-126">-소유자</span><span class="sxs-lookup"><span data-stu-id="e21ec-126">-Owner</span></span>
<span data-ttu-id="e21ec-127">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e21ec-128">-ResourceId</span></span>
<span data-ttu-id="e21ec-129">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-129">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e21ec-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e21ec-131">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-132">-상태</span><span class="sxs-lookup"><span data-stu-id="e21ec-132">-State</span></span>
<span data-ttu-id="e21ec-133">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e21ec-134">-SubscriptionId</span></span>
<span data-ttu-id="e21ec-135">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e21ec-136">-TenantId</span></span>
<span data-ttu-id="e21ec-137">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-138">-확인</span><span class="sxs-lookup"><span data-stu-id="e21ec-138">-Confirm</span></span>
<span data-ttu-id="e21ec-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21ec-140">-WhatIf</span></span>
<span data-ttu-id="e21ec-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e21ec-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21ec-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21ec-143">CommonParameters</span></span>
<span data-ttu-id="e21ec-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21ec-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21ec-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e21ec-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21ec-146">입력</span><span class="sxs-lookup"><span data-stu-id="e21ec-146">INPUTS</span></span>

## <span data-ttu-id="e21ec-147">출력</span><span class="sxs-lookup"><span data-stu-id="e21ec-147">OUTPUTS</span></span>

### <span data-ttu-id="e21ec-148">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="e21ec-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="e21ec-149">상속자</span><span class="sxs-lookup"><span data-stu-id="e21ec-149">NOTES</span></span>

## <span data-ttu-id="e21ec-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e21ec-150">RELATED LINKS</span></span>
