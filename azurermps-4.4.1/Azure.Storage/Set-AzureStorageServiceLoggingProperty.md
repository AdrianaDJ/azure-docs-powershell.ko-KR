---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535571"
---
# Set-AzureStorageServiceLoggingProperty

## SYNOPSIS
Azure Storage 서비스에 대 한 로깅을 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## 설명은
**AzureStorageServiceLoggingProperty** Cmdlet은 Azure Storage 서비스에 대 한 로깅을 수정 합니다.

## 예제의

### 예제 1: Blob 서비스에 대 한 로깅 속성 수정
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

이 명령은 blob 저장소에 대 한 버전 1.0 로깅을 수정 하 여 읽기 및 쓰기 작업을 포함 합니다.
Azure 저장소 서비스 로깅은 10 일 동안 항목을 유지 합니다.
이 명령은 *PassThru* 매개 변수를 지정 하므로,이 명령은 수정 된 로깅 속성을 표시 합니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -LoggingOperations
Azure 저장소 서비스 작업의 배열을 지정 합니다.
Azure 저장소 서비스는이 매개 변수에서 지정 하는 작업을 기록 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 않아야
- 자세한
- 작성
- 삭제
- 모든

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이 업데이트 된 로깅 속성을 반환 함을 나타냅니다.
이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -보존 기간
Azure 저장소 서비스에서 기록 된 정보를 유지 하는 일 수를 지정 합니다.

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

### -ServiceType
저장소 서비스 유형을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형에 대 한 로깅 속성을 수정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 블 
- 테이블로
- 전담팀
- 파일

현재 파일의 값이 지원 되지 않습니다.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -버전
Azure 저장소 서비스 로깅 버전을 지정 합니다.
기본값은 1.0입니다.

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### IStorageContext

' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.

## 출력

### WindowsAzure. LoggingProperties를 저장 합니다.

## 상속자

## 관련 링크

[Get-AzureStorageServiceLoggingProperty](./Get-AzureStorageServiceLoggingProperty.md)

[새로운 AzureStorageContext](./New-AzureStorageContext.md)


