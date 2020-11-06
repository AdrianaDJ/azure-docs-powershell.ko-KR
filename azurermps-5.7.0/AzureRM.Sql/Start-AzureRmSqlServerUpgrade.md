---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d33635cd3876a3426c3db96489d623d0a61f1d03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532599"
---
# <span data-ttu-id="4fde8-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4fde8-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="4fde8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fde8-102">SYNOPSIS</span></span>
<span data-ttu-id="4fde8-103">SQL 데이터베이스 서버의 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fde8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fde8-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fde8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fde8-105">DESCRIPTION</span></span>
<span data-ttu-id="4fde8-106">**AzureRmSqlServerUpgrade** Cmdlet은 Azure SQL 데이터베이스 서버 버전 11을 버전 12로 업그레이드 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="4fde8-107">Get-AzureRmSqlServerUpgrade cmdlet을 사용 하 여 업그레이드 진행률을 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="4fde8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4fde8-108">EXAMPLES</span></span>

### <span data-ttu-id="4fde8-109">예제 1: 서버 업그레이드</span><span class="sxs-lookup"><span data-stu-id="4fde8-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="4fde8-110">이 명령은 리소스 그룹 TesourceGroup01에 할당 된 server01 이라는 서버를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="4fde8-111">예제 2: 일정 시간 및 데이터베이스 권장 구성을 사용 하 여 서버 업그레이드</span><span class="sxs-lookup"><span data-stu-id="4fde8-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="4fde8-112">첫 번째 명령은 Get-Date cmdlet을 사용 하 여 5 분 후에 시간을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="4fde8-113">이 명령은 $ScheduleTime 변수에 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="4fde8-114">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="4fde8-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="4fde8-115">두 번째 명령은 **RecommendedDatabaseProperties** 개체를 만든 다음이 개체를 변수 $DatabaseMap에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>

<span data-ttu-id="4fde8-116">다음 세 개의 명령은 $DatabaseMap에 저장 된 개체의 속성에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>

<span data-ttu-id="4fde8-117">마지막 명령은 Server01 이라는 기존 서버를 버전 12.0으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="4fde8-118">가장 빠른 업그레이드 시간은 $ScheduleTime 변수에 지정 된 대로 명령을 실행 한 후 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="4fde8-119">업그레이드 후 데이터베이스 contosodb는 표준 버전을 실행 하 고 서비스 수준 목표가 S0으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="4fde8-120">변수</span><span class="sxs-lookup"><span data-stu-id="4fde8-120">PARAMETERS</span></span>

### <span data-ttu-id="4fde8-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="4fde8-121">-DatabaseCollection</span></span>
<span data-ttu-id="4fde8-122">이 cmdlet에서 서버 업그레이드에 사용 하는 **RecommendedDatabaseProperties** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fde8-123">-DefaultProfile</span></span>
<span data-ttu-id="4fde8-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4fde8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="4fde8-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="4fde8-126">서버 업그레이드에 사용할 **UpgradeRecommendedElasticPoolProperties** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fde8-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fde8-128">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-128">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="4fde8-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="4fde8-130">빠른 시간을 **DateTime** 개체로 지정 하 여 서버를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="4fde8-131">UTC (협정 세계시)로 ISO8601 형식으로 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="4fde8-132">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="4fde8-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4fde8-133">-ServerName</span></span>
<span data-ttu-id="4fde8-134">이 cmdlet이 업그레이드 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="4fde8-135">-ServerVersion</span></span>
<span data-ttu-id="4fde8-136">이 cmdlet에서 서버를 업그레이드할 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="4fde8-137">유일 하 게 유효한 값은 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-137">The only valid value is 12.0.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fde8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fde8-138">CommonParameters</span></span>
<span data-ttu-id="4fde8-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fde8-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fde8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fde8-141">입력</span><span class="sxs-lookup"><span data-stu-id="4fde8-141">INPUTS</span></span>

### <span data-ttu-id="4fde8-142">않아야</span><span class="sxs-lookup"><span data-stu-id="4fde8-142">None</span></span>
<span data-ttu-id="4fde8-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fde8-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fde8-144">출력</span><span class="sxs-lookup"><span data-stu-id="4fde8-144">OUTPUTS</span></span>

### <span data-ttu-id="4fde8-145">AzureSqlServerUpgradeModel 업그레이드. 모델. m a.</span><span class="sxs-lookup"><span data-stu-id="4fde8-145">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="4fde8-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4fde8-146">NOTES</span></span>

## <span data-ttu-id="4fde8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fde8-147">RELATED LINKS</span></span>

[<span data-ttu-id="4fde8-148">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4fde8-148">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4fde8-149">중지-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4fde8-149">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4fde8-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="4fde8-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

