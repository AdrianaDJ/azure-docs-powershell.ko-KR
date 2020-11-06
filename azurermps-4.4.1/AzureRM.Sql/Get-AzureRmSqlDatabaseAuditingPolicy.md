---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a6fe2e171338885af2367d6fec1cc3a97002b321
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536939"
---
# <span data-ttu-id="11f25-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="11f25-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="11f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f25-102">SYNOPSIS</span></span>
<span data-ttu-id="11f25-103">데이터베이스의 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11f25-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11f25-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11f25-105">DESCRIPTION</span></span>
<span data-ttu-id="11f25-106">**AzureRmSqlDatabaseAuditingPolicy** Cmdlet은 Azure SQL 데이터베이스의 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="11f25-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="11f25-108">예제의</span><span class="sxs-lookup"><span data-stu-id="11f25-108">EXAMPLES</span></span>

### <span data-ttu-id="11f25-109">예제 1: 테이블 감사가 정의 된 Azure SQL 데이터베이스의 감사 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="11f25-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="11f25-110">예제 2: Blob 감사가 정의 된 Azure SQL 데이터베이스의 감사 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="11f25-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="11f25-111">변수</span><span class="sxs-lookup"><span data-stu-id="11f25-111">PARAMETERS</span></span>

### <span data-ttu-id="11f25-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11f25-112">-DatabaseName</span></span>
<span data-ttu-id="11f25-113">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-113">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="11f25-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f25-114">-ResourceGroupName</span></span>
<span data-ttu-id="11f25-115">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-115">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="11f25-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11f25-116">-ServerName</span></span>
<span data-ttu-id="11f25-117">데이터베이스가 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-117">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="11f25-118">-확인</span><span class="sxs-lookup"><span data-stu-id="11f25-118">-Confirm</span></span>
<span data-ttu-id="11f25-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f25-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f25-120">-WhatIf</span></span>
<span data-ttu-id="11f25-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11f25-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f25-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f25-123">-DefaultProfile</span></span>
<span data-ttu-id="11f25-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f25-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f25-125">CommonParameters</span></span>
<span data-ttu-id="11f25-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f25-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f25-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f25-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f25-128">입력</span><span class="sxs-lookup"><span data-stu-id="11f25-128">INPUTS</span></span>

## <span data-ttu-id="11f25-129">출력</span><span class="sxs-lookup"><span data-stu-id="11f25-129">OUTPUTS</span></span>

### <span data-ttu-id="11f25-130">Microsoft. \*. \* DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="11f25-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="11f25-131">상속자</span><span class="sxs-lookup"><span data-stu-id="11f25-131">NOTES</span></span>

## <span data-ttu-id="11f25-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11f25-132">RELATED LINKS</span></span>

[<span data-ttu-id="11f25-133">제거-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="11f25-133">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="11f25-134">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="11f25-134">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)


