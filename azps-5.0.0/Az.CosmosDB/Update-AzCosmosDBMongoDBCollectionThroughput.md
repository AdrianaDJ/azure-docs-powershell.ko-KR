---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306788"
---
# <span data-ttu-id="6887a-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="6887a-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="6887a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6887a-102">SYNOPSIS</span></span>
<span data-ttu-id="6887a-103">CosmosDB MongoDB Collection의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6887a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6887a-104">SYNTAX</span></span>

### <span data-ttu-id="6887a-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6887a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6887a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6887a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6887a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6887a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6887a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6887a-108">DESCRIPTION</span></span>
<span data-ttu-id="6887a-109">CosmosDB MongoDB Collection의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6887a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6887a-110">EXAMPLES</span></span>

### <span data-ttu-id="6887a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6887a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="6887a-112">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="6887a-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="6887a-113">변수</span><span class="sxs-lookup"><span data-stu-id="6887a-113">PARAMETERS</span></span>

### <span data-ttu-id="6887a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6887a-114">-AccountName</span></span>
<span data-ttu-id="6887a-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-115">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6887a-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6887a-117">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-117">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-118">-확인</span><span class="sxs-lookup"><span data-stu-id="6887a-118">-Confirm</span></span>
<span data-ttu-id="6887a-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6887a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6887a-120">-DatabaseName</span></span>
<span data-ttu-id="6887a-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6887a-122">-DefaultProfile</span></span>
<span data-ttu-id="6887a-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6887a-124">-InputObject</span></span>
<span data-ttu-id="6887a-125">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-126">-이름</span><span class="sxs-lookup"><span data-stu-id="6887a-126">-Name</span></span>
<span data-ttu-id="6887a-127">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-127">Collection name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6887a-128">-ParentObject</span></span>
<span data-ttu-id="6887a-129">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6887a-130">-ResourceGroupName</span></span>
<span data-ttu-id="6887a-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-131">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-132">-처리량</span><span class="sxs-lookup"><span data-stu-id="6887a-132">-Throughput</span></span>
<span data-ttu-id="6887a-133">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="6887a-134">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-134">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6887a-135">-WhatIf</span></span>
<span data-ttu-id="6887a-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6887a-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6887a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6887a-138">CommonParameters</span></span>
<span data-ttu-id="6887a-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6887a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6887a-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6887a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6887a-141">입력</span><span class="sxs-lookup"><span data-stu-id="6887a-141">INPUTS</span></span>

### <span data-ttu-id="6887a-142">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6887a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="6887a-143">출력</span><span class="sxs-lookup"><span data-stu-id="6887a-143">OUTPUTS</span></span>

### <span data-ttu-id="6887a-144">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6887a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6887a-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6887a-145">NOTES</span></span>

## <span data-ttu-id="6887a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6887a-146">RELATED LINKS</span></span>