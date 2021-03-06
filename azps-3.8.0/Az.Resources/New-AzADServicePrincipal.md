---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f921cceb3692032f61f99db825efeea074773faa
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94311717"
---
# New-AzADServicePrincipal

## SYNOPSIS
새 azure active directory service principal을 만듭니다.

## 구문과

### SimpleParameterSet (기본값)
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
새 azure active directory service principal을 만듭니다. 사용자가 매개 변수에 대 한 기본값을 제공 하지 않는 경우 기본 매개 변수 집합에는 기본 값이 사용 됩니다. 사용 되는 기본값에 대 한 자세한 내용은 아래의 해당 매개 변수에 대 한 설명을 참조 하세요.
이 cmdlet에는 and 매개 변수를 사용 하 여 서비스 사용자에 게 역할을 할당 하는 기능이 있습니다 `Role` `Scope` . 이러한 매개 변수 중 하나도 제공 하지 않으면 서비스 사용자에 게 역할이 할당 되지 않습니다. `Role`And `Scope` 매개 변수의 기본값은 각각 "참가자"이 고, 현재 구독은 사용자가 두 매개 _note_ 변수 중 하나에 대 한 값을 제공 하는 경우에만 사용 됩니다.
또한 cmdlet은 응용 프로그램을 암시적으로 만들고 해당 속성 (ApplicationId이 제공 되지 않은 경우)을 설정 합니다. 응용 프로그램별 매개 변수를 업데이트 하려면 Set-AzADApplication cmdlet을 사용 하세요.

> [!WARNING]
> **새-AzADServicePrincipal** 명령을 사용 하 여 서비스 사용자를 만드는 경우 출력에는 보호 해야 하는 자격 증명이 포함 됩니다. 이러한 자격 증명을 코드에 포함 하지 않도록 하거나 자격 증명을 소스 제어에 체크 인해야 합니다. 다른 방법으로는 자격 증명을 사용할 필요가 없도록 [관리 되는 id](/azure/active-directory/managed-identities-azure-resources/overview) 를 사용 하는 것이 좋습니다.
>
> 기본적으로 **AzADServicePrincipal** 는 구독 범위에서 [참가자](/azure/role-based-access-control/built-in-roles#contributor) 역할을 서비스 사용자에 게 할당 합니다. 손상 된 서비스 보안 주체의 위험을 줄이려면 더 구체적인 역할을 할당 하 고 리소스 또는 리소스 그룹으로 범위를 좁힙니다. 자세한 내용은 [역할 할당을 추가 하는 단계를](/azure/role-based-access-control/role-assignments-steps) 참조 하세요.

## 예제의

### 예제 1-간단한 광고 서비스 사용자 만들기

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다. 응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다. Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.

### 예제 2-지정 된 역할 및 기본 범위의 간단한 광고 서비스 사용자 만들기

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다. 응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다. 서비스 사용자가 현재 구독에 대해 "읽기" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Scope` ).

### 예제 3-지정 된 범위 및 기본 역할을 가진 간단한 광고 서비스 사용자 만들기

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다. 응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다. 제공 된 리소스 그룹 범위를 통해 서비스 사용자가 "참가자" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Role` ).

### 예제 4-단순 광고 서비스 주도자 만들기 지정 된 범위 및 역할

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다. 응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다. 서비스 사용자가 제공 된 리소스 그룹 범위에 대해 "읽기" 권한을 사용 하 여 만들어졌습니다.

### 예제 5-역할을 할당 하 여 응용 프로그램 id를 사용 하 여 새 광고 서비스 사용자 만들기

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

응용 프로그램 id가 ' 4a28ad2-3| 4-4a41-bc3b-d22ddf90000e ' 인 응용 프로그램에 대 한 새 광고 서비스 사용자를 만듭니다. Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.

### 예제 6-파이핑을 사용 하 여 새 광고 서비스 사용자 만들기

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

개체 id가 ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' 인 응용 프로그램을 가져오고 해당 응용 프로그램에 대 한 새 광고 서비스 사용자를 만들기 위해 New-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.

### 예제 7-DisplayName 및 password 자격 증명을 사용 하 여 새 광고 서비스 사용자 만들기

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

이름이 "ServicePrincipalName"이 고 암호가 "StrongPassworld! 23" 인 새 응용 프로그램을 만들고 방금 만든 응용 프로그램을 기반으로 서비스 사용자를 만듭니다. 시작 날짜 및 종료 날짜가 암호 자격 증명에 추가 됩니다.

### 예제 8-DisplayName 및 일반 키 자격 증명을 사용 하 여 새 광고 서비스 사용자 만들기

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

이름이 "ServicePrincipalName"이 고 certifcate "$cert" 인 새 응용 프로그램을 만들고 방금 만든 응용 프로그램을 기반으로 서비스 사용자를 만듭니다. 끝 날짜가 키 자격 증명에 추가 됩니다.

## 변수

### -ApplicationId
테 넌 트의 서비스 사용자에 대 한 고유한 응용 프로그램 id입니다.
만든 후에는이 속성을 변경할 수 없습니다.
응용 프로그램 id가 지정 되지 않은 경우 생성 됩니다.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject
서비스 사용자를 만들 응용 프로그램을 나타내는 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue
"비대칭" 자격 증명 형식의 값입니다.
Base 64 인코딩된 인증서를 나타냅니다.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
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

### -DisplayName
서비스 사용자의 식별 이름입니다. 표시 이름이 제공 되지 않은 경우이 값은 기본적으로 ' azure-powershell-MM-dd-yyyy-mm-dd-ss ' 이며, 여기서 접미사는 응용 프로그램을 만드는 데 걸리는 시간입니다.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
자격 증명 사용의 유효 종료 날짜입니다.
기본 끝 날짜 값은 오늘부터 1 년입니다. "비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential
응용 프로그램과 연결 된 키 자격 증명의 컬렉션입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential
응용 프로그램과 연결 된 암호 자격 증명 모음입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -역할
서비스 사용자가 범위를 초과 하는 역할입니다. 값이 `Scope` 제공 되지만 값이 제공 되지 않으면 `Role` 기본적으로 `Role` ' 참가자 ' 역할이 지정 됩니다.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -범위
서비스 사용자에 게 사용 권한이 있는 범위입니다. 값이 `Role` 제공 되지만 값이 제공 되지 않으면 `Scope` `Scope` 현재 구독이 기본값으로 지정 됩니다.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment
설정 하는 경우 서비스 사용자에 대 한 기본 역할 할당 만들기를 건너뜁니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -시작 날짜
자격 증명 사용의 유효 시작 날짜입니다.
기본 시작 날짜 값은 오늘입니다. "비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 시스템 Guid

### System. 문자열

### ActiveDirectory PSADApplication 프로그램

### ActiveDirectory PSADPasswordCredential []

### ActiveDirectory PSADKeyCredential []

### 시스템. 날짜/시간

## 출력

### ActiveDirectory PSADServicePrincipal

### PSADServicePrincipalWrapper에 대 한 권한 부여.

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포

## 관련 링크

[제거-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[새로운 AzADApplication](./New-AzADApplication.md)

[제거-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[새로운 AzADSpCredential](./New-AzADSpCredential.md)

[제거-AzADSpCredential](./Remove-AzADSpCredential.md)

