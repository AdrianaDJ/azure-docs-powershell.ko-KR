---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305873"
---
# Get-AzDataLakeAnalyticsCatalogItem

## SYNOPSIS
Data Lake Analytics 카탈로그 항목 또는 항목 유형을 가져옵니다.

## 구문과

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDataLakeAnalyticsCatalogItem** 에서 지정 된 Azure Data Lake Analytics 카탈로그 항목을 가져오거나 지정 된 형식의 카탈로그 항목을 가져옵니다.

## 예제의

### 예제 1: 지정 된 데이터베이스 가져오기
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

이 명령은 지정 된 데이터베이스를 가져옵니다.

### 예제 2: 지정 된 데이터베이스 및 스키마의 테이블 가져오기
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

이 명령은 지정 된 데이터베이스의 테이블 목록을 가져옵니다.

## 변수

### -계정
Data Lake Analytics 계정 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -ItemType
가져오고 나열 되는 항목의 카탈로그 항목 형식을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 데이터
- 스키마
- 어셈블리가
- 테이블로
- Table의 Edfunction
- TableStatistics
- ExternalDataSource
- 보려고
- 절차
- 기밀
- 자격 증명
- 형식
- TablePartition

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
검색할 항목에 대 한 다중 파트 경로를 지정 하거나 나열할 항목의 상위 항목에 대 한 여러 부분으로 구성 되어 있습니다.
경로의 각 부분은 마침표 (.)로 구분 되어야 합니다.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### DataLakeAnalytics. DataLakeAnalyticsEnums + CatalogItemType.

### DataLakeAnalytics. CatalogPathInstance/.

## 출력

### DataLake. CatalogItem-. *

## 상속자

## 관련 링크

[테스트-AzDataLakeAnalyticsCatalogItem](./Test-AzDataLakeAnalyticsCatalogItem.md)


