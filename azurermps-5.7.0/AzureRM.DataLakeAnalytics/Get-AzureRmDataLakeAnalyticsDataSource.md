---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525152"
---
# Get-AzureRmDataLakeAnalyticsDataSource

## SYNOPSIS
Data Lake Analytics 데이터 원본을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### GetAllDataSources 원본 (기본값)
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetDataLakeStoreAccount
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBlobStorageAccount
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 데이터 원본을 가져옵니다.

## 예제의

### 예제 1: 계정에서 데이터 원본 가져오기
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

이 명령은 Data Lake Analytics 계정에서 ContosoAdls 이라는 Data Lake Store 데이터 원본을 가져옵니다.

### 예제 2: Data Lake Analytics 계정에서 Data Lake Store 계정 목록 가져오기
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

이 명령은 Data Lake Analytics 계정에서 모든 Data Lake Store 계정을 가져옵니다.

## 변수

### -계정
이 cmdlet이 데이터 원본을 가져오는 데이터 호수 분석 계정을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Blob
Azure Blob 저장소 데이터 원본의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataLakeStore
Data Lake Store 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -ResourceGroupName
데이터 원본을 포함 하는 리소스 그룹 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### PSStorageAccountInfo
지정 된 Azure Storage 계정 세부 정보입니다.

### PSDataLakeStoreAccountInfo
지정 된 Data Lake Store 계정 세부 정보

### 목록<AdlDataSource>
지정 된 Data Lake Analytics 계정의 Azure 저장소 계정 및 Data Lake Store 계정 목록입니다.

## 상속자

## 관련 링크

[추가-AzureRmDataLakeAnalyticsDataSource](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[제거-AzureRmDataLakeAnalyticsDataSource](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[Set-AzureRmDataLakeAnalyticsDataSource](./Set-AzureRmDataLakeAnalyticsDataSource.md)

