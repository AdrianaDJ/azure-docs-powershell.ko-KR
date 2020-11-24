---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308945"
---
# <span data-ttu-id="1a54f-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="1a54f-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="1a54f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a54f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a54f-103">Redis Cache에 대 한 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="1a54f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a54f-104">SYNTAX</span></span>

### <span data-ttu-id="1a54f-105">All링크 Forcache (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a54f-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a54f-106">All링크 Forprimarycache</span><span class="sxs-lookup"><span data-stu-id="1a54f-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a54f-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="1a54f-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a54f-108">All링크 Forsecondarycache</span><span class="sxs-lookup"><span data-stu-id="1a54f-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a54f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1a54f-109">DESCRIPTION</span></span>
<span data-ttu-id="1a54f-110">지리적 복제 링크 세부 정보는 네 가지 방법으로 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="1a54f-111">매개 변수 이름 또는 PrimaryServerName 및/또는 SecondaryServerName을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="1a54f-112">Name이 지정 되 면 캐시가 존재 하는 모든 링크가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="1a54f-113">PrimaryServerName만 지정 하는 경우 캐시가 기본으로 있는 모든 링크는 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="1a54f-114">SecondaryServerName만 지정 하는 경우 캐시가 보조 인 모든 링크는 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="1a54f-115">PrimaryServerName 및 SecondaryServerName이 모두 지정 된 경우 올바른 역할의 특정 링크가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="1a54f-116">예제의</span><span class="sxs-lookup"><span data-stu-id="1a54f-116">EXAMPLES</span></span>

### <span data-ttu-id="1a54f-117">예제 1: using 매개 변수 설정 가져오기 All링크 Forcache</span><span class="sxs-lookup"><span data-stu-id="1a54f-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="1a54f-118">이 명령은 mycache1 이라는 Redis Cache에 대 한 모든 지역/복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="1a54f-119">예제 2: using 매개 변수 설정 가져오기 All링크 Forprimarycache</span><span class="sxs-lookup"><span data-stu-id="1a54f-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="1a54f-120">이 명령은 mycache1 이라는 Redis 캐시가 기본 인 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="1a54f-121">예제 3: 사용 하는 매개 변수 설정 Get Allindex Forsecondarycache</span><span class="sxs-lookup"><span data-stu-id="1a54f-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="1a54f-122">이 명령은 mycache2 이라는 Redis 캐시가 보조 인 지역 복제 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="1a54f-123">예제 4: SingleLink set 매개 변수를 사용 하 여 가져오기</span><span class="sxs-lookup"><span data-stu-id="1a54f-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="1a54f-124">이 명령은 mycache1 이라는 Redis 캐시가 기본 인 단일 지역 복제 링크와 mycache2 이라는 Redis Cache를 보조로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="1a54f-125">변수</span><span class="sxs-lookup"><span data-stu-id="1a54f-125">PARAMETERS</span></span>

### <span data-ttu-id="1a54f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a54f-126">-DefaultProfile</span></span>
<span data-ttu-id="1a54f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a54f-128">-이름</span><span class="sxs-lookup"><span data-stu-id="1a54f-128">-Name</span></span>
<span data-ttu-id="1a54f-129">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a54f-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="1a54f-130">-PrimaryServerName</span></span>
<span data-ttu-id="1a54f-131">Link의 기본 redis cache 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a54f-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="1a54f-132">-SecondaryServerName</span></span>
<span data-ttu-id="1a54f-133">Link의 보조 redis 캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a54f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a54f-134">CommonParameters</span></span>
<span data-ttu-id="1a54f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a54f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a54f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a54f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a54f-137">입력</span><span class="sxs-lookup"><span data-stu-id="1a54f-137">INPUTS</span></span>

### <span data-ttu-id="1a54f-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a54f-138">System.String</span></span>

## <span data-ttu-id="1a54f-139">출력</span><span class="sxs-lookup"><span data-stu-id="1a54f-139">OUTPUTS</span></span>

### <span data-ttu-id="1a54f-140">PSRedisLinkedServer. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="1a54f-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="1a54f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1a54f-141">NOTES</span></span>

## <span data-ttu-id="1a54f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a54f-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a54f-143">새로운 AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="1a54f-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="1a54f-144">제거-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="1a54f-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="1a54f-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a54f-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1a54f-146">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a54f-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1a54f-147">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a54f-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1a54f-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1a54f-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)