---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 219ff64309cc11fd5e65d614f67d2d531737c8b1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882146"
---
# Get-AzureRmRoleDefinition

## SYNOPSIS
할당에 사용할 수 있는 모든 Azure RBAC 역할을 나열 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### RoleDefinitionNameParameterSet
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionIdParameterSet
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
특정 역할 이름과 함께 Get-AzureRmRoleDefinition 명령을 사용 하 여 세부 정보를 확인 합니다.
역할이 액세스를 허용 하는 개별 작업을 검사 하려면 해당 역할의 작업 및 NotActions 속성을 검토 합니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

읽기 프로그램 역할 정의 가져오기

### 예제 2
```
PS C:\> Get-AzureRmRoleDefinition
```

모든 RBAC 역할 정의를 나열 합니다.

## 변수

### -사용자 지정
지정 된 경우 디렉터리에 사용자 지정 만들기 역할만 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
역할 정의 Id입니다.

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
역할 정의 이름입니다.
예를 들어 독자, 참가자, 가상 컴퓨터 참가자.

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -범위
역할 정의 범위

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
매개 변수: Scope (ByValue)

### 시스템 Guid

### System.webserver 매개 변수

## 출력

### Microsoft. a. PSRoleDefinition (.Resources.

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포

## 관련 링크

[새로운 AzureRmRoleAssignment](./New-AzureRmRoleAssignment.md)

[Get-AzureRmRoleAssignment](./Get-AzureRmRoleAssignment.md)

[새로운 AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[제거-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

