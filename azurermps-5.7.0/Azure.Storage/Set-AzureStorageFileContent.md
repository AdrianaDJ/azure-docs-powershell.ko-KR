---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 5f2aed68aea9f97b3dd66a5322d332d4666c081e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711737"
---
# Set-AzureStorageFileContent

## SYNOPSIS
파일의 내용을 업로드 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ShareName (기본값)
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 공유
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 디렉토리로
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureStorageFileContent** cmdlet은 지정 된 공유에서 파일의 콘텐츠를 파일에 업로드 합니다.

## 예제의

### 예제 1: 현재 폴더에 파일 업로드
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

이 명령은 현재 폴더에 DataFile37 이라는 파일을 ContosoWorkingFolder 이라는 폴더에 있는 CurrentDataFile 파일 이라는 파일로 업로드 합니다.

### 예제 2: 현재 폴더의 모든 파일 업로드
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

이 예제에서는 여러 가지 일반적인 Windows PowerShell cmdlet 및 현재 cmdlet을 사용 하 여 현재 폴더의 모든 파일을 컨테이너 ContosoShare06의 루트 폴더에 업로드 합니다.

첫 번째 명령은 현재 폴더의 이름을 가져와 $CurrentFolder 변수에 저장 합니다.

두 번째 명령은 **AzureStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고이를 $Container 변수에 저장 합니다.

마지막 명령은 파이프라인 연산자를 사용 하 여 현재 폴더의 콘텐츠를 가져와 각 항목을 Where-Object cmdlet에 전달 합니다.
해당 cmdlet은 파일이 아닌 개체를 필터링 한 다음 파일을 ForEach-Object cmdlet에 전달 합니다.
해당 cmdlet은 해당 경로를 만드는 각 파일에 대해 스크립트 블록을 실행 한 다음 현재 cmdlet을 사용 하 여 파일을 업로드 합니다.
결과는이 예제에서 업로드 하는 다른 파일과 관련 하 여 동일한 이름과 상대 위치를 갖습니다.
스크립트 블록에 대 한 자세한 내용을 보려면을 입력 `Get-Help about_Script_Blocks` 합니다.

## 변수

### -ClientTimeoutPerRequest
한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.
이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.
이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.

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

### -ConcurrentTaskCount
최대 동시 네트워크 통화를 지정 합니다.
이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.
지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.
이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
기본값은 10입니다.

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

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -디렉터리
폴더를 **Cloudfiledirectory** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 폴더에 파일을 업로드 합니다.
디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.
또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
이 cmdlet이 기존 Azure 저장소 파일을 덮어쓴다는 것을 나타냅니다.

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

### -PassThru
이 cmdlet이 생성 또는 업로드 하는 **AzureStorageFile** 개체를 반환 함을 나타냅니다.

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

### -Path
파일 또는 폴더의 경로를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 또는이 매개 변수에서 지정 하는 폴더의 파일에 콘텐츠를 업로드 합니다.
폴더를 지정 하는 경우이 cmdlet은 원본 파일과 동일한 이름을 가진 파일을 만듭니다.

존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 해당 파일에 콘텐츠를 저장 합니다.
이미 존재 하는 파일을 지정 하 고 _Force_ 매개 변수를 지정 하면이 cmdlet이 파일의 내용을 덮어씁니다.
이미 존재 하 고 _Force_ 를 지정 하지 않은 파일을 지정 하면이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.

존재 하지 않는 폴더의 경로를 지정 하면이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.

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

### -공유
**Cloudfileshare** 되지 않는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 공유의 파일에 업로드 합니다.
**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.
이 개체는 저장소 컨텍스트를 포함 합니다.
이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ShareName
파일 공유의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 공유의 파일에 업로드 합니다.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -원본
이 cmdlet이 업로드 하는 원본 파일을 지정 합니다.
존재 하지 않는 파일을 지정 하면이 cmdlet은 오류를 반환 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### IStorageContext

' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.

### CloudFileDirectory

' Directory ' 매개 변수는 파이프라인에서 ' CloudFileDirectory ' 형식의 값을 허용 합니다.

### CloudFileShare

' Share ' 매개 변수는 파이프라인에서 ' CloudFileShare 범위 ' 형식의 값을 받아들입니다.

## 출력

## 상속자

## 관련 링크

[-AzureStorageDirectory 제거](./Remove-AzureStorageDirectory.md)

[새-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)
