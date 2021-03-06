---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 07bc19bd2314164b37ec9e014f5cad68de97d21f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529408"
---
# Remove-AzureRmADServicePrincipal

## SYNOPSIS
Azure active directory 서비스 사용자를 삭제 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ObjectIdParameterSet (기본값)
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNParameterSet
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Azure active directory 서비스 사용자를 삭제 합니다.

## 예제의

### 예제 1-개체 id 별 서비스 사용자 제거

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

개체 id가 ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' 인 서비스 사용자를 제거 합니다.

### 예제 2-응용 프로그램 id로 서비스 사용자 제거

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

응용 프로그램 id가 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 인 서비스 사용자를 제거 합니다.

### 예제 3-SPN에서 서비스 사용자 제거

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

서비스 사용자 이름이 "MyServicePrincipal" 인 서비스 사용자를 제거 합니다.

### 예제 4-파이핑을 통해 서비스 사용자 제거

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

개체 id가 ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' 인 서비스 사용자를 가져오고 해당 서비스 사용자를 제거 하기 위해 Remove-AzureRmADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.

### 예제 5-응용 프로그램을 파이핑 하 여 서비스 사용자 제거

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

응용 프로그램 id가 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 인 응용 프로그램을 가져오고 해당 응용 프로그램과 연결 된 서비스 사용자를 제거 하기 위해 Remove-AzureRmADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.

## 변수

### -ApplicationId
서비스 사용자 응용 프로그램 id입니다.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
서비스 사용자가 제거 되 고 있는 응용 프로그램 개체입니다.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -DisplayName
서비스 주체의 표시 이름입니다.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
확인 하지 않고 서비스 사용자 삭제로 전환 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
서비스 사용자 개체입니다.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
삭제할 서비스 주체의 개체 id입니다.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
지정 된 경우 삭제 된 서비스 사용자를 반환 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipalName
서비스 사용자 이름입니다.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 시스템 Guid

### System. 문자열

### Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adserviceprincipal
매개 변수: InputObject (ByValue)

### Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication
매개 변수: ApplicationObject (ByValue)

## 출력

### Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adserviceprincipal

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포

## 관련 링크

[새로운 AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

[Set-AzureRmADServicePrincipal](./Set-AzureRmADServicePrincipal.md)

[제거-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[제거-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)
