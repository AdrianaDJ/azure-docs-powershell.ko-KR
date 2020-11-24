---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306734"
---
# <span data-ttu-id="85469-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="85469-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="85469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85469-102">SYNOPSIS</span></span>
<span data-ttu-id="85469-103">CosmosDB Sql 트리거를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="85469-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="85469-104">기존 트리거를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="85469-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="85469-105">구문과</span><span class="sxs-lookup"><span data-stu-id="85469-105">SYNTAX</span></span>

### <span data-ttu-id="85469-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="85469-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85469-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85469-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85469-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85469-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85469-109">설명은</span><span class="sxs-lookup"><span data-stu-id="85469-109">DESCRIPTION</span></span>
<span data-ttu-id="85469-110">CosmosDB Sql 트리거를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="85469-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="85469-111">기존 트리거를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="85469-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="85469-112">예제의</span><span class="sxs-lookup"><span data-stu-id="85469-112">EXAMPLES</span></span>

### <span data-ttu-id="85469-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="85469-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="85469-114">변수</span><span class="sxs-lookup"><span data-stu-id="85469-114">PARAMETERS</span></span>

### <span data-ttu-id="85469-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85469-115">-AccountName</span></span>
<span data-ttu-id="85469-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="85469-117">-본문</span><span class="sxs-lookup"><span data-stu-id="85469-117">-Body</span></span>
<span data-ttu-id="85469-118">트리거의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="85469-119">-확인</span><span class="sxs-lookup"><span data-stu-id="85469-119">-Confirm</span></span>
<span data-ttu-id="85469-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85469-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85469-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="85469-121">-ContainerName</span></span>
<span data-ttu-id="85469-122">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-122">Container name.</span></span>

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

### <span data-ttu-id="85469-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="85469-123">-DatabaseName</span></span>
<span data-ttu-id="85469-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-124">Database name.</span></span>

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

### <span data-ttu-id="85469-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85469-125">-DefaultProfile</span></span>
<span data-ttu-id="85469-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85469-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85469-127">-InputObject</span></span>
<span data-ttu-id="85469-128">Sql 트리거 개체</span><span class="sxs-lookup"><span data-stu-id="85469-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85469-129">-이름</span><span class="sxs-lookup"><span data-stu-id="85469-129">-Name</span></span>
<span data-ttu-id="85469-130">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-130">Trigger name.</span></span>

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

### <span data-ttu-id="85469-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="85469-131">-ParentObject</span></span>
<span data-ttu-id="85469-132">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="85469-132">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85469-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85469-133">-ResourceGroupName</span></span>
<span data-ttu-id="85469-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-134">Name of resource group.</span></span>

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

### <span data-ttu-id="85469-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="85469-135">-TriggerOperation</span></span>
<span data-ttu-id="85469-136">트리거가 연결 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="85469-137">사용할 수 있는 값은 다음과 같습니다. ' All ', ' Create ', ' Update ', ' Delete ', ' Replace '</span><span class="sxs-lookup"><span data-stu-id="85469-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="85469-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="85469-138">-TriggerType</span></span>
<span data-ttu-id="85469-139">트리거의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="85469-139">Type of the Trigger.</span></span>
<span data-ttu-id="85469-140">사용할 수 있는 값은 다음과 같습니다. ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="85469-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="85469-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85469-141">-WhatIf</span></span>
<span data-ttu-id="85469-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85469-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85469-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85469-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85469-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85469-144">CommonParameters</span></span>
<span data-ttu-id="85469-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85469-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85469-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85469-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85469-147">입력</span><span class="sxs-lookup"><span data-stu-id="85469-147">INPUTS</span></span>

### <span data-ttu-id="85469-148">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="85469-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="85469-149">CosmosDB. PSSqlTriggerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="85469-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="85469-150">출력</span><span class="sxs-lookup"><span data-stu-id="85469-150">OUTPUTS</span></span>

### <span data-ttu-id="85469-151">CosmosDB. PSSqlTriggerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="85469-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="85469-152">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="85469-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="85469-153">상속자</span><span class="sxs-lookup"><span data-stu-id="85469-153">NOTES</span></span>

## <span data-ttu-id="85469-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85469-154">RELATED LINKS</span></span>