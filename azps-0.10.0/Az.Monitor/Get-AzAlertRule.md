---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 01774d80ce422c1ac0a48df61d44328b6b5b0105
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875789"
---
# Get-AzAlertRule

## SYNOPSIS
알림 규칙을 가져옵니다.

## 구문과

### GetByResourceGroup
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceUri
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzAlertRule** cmdlet은 이름 또는 URI 또는 지정 된 리소스 그룹의 모든 알림 규칙을 기준으로 경고 규칙을 가져옵니다.

## 예제의

### 예제 1: 리소스 그룹에 대 한 알림 규칙 가져오기
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

이 명령은 Default-CentralUS 이라는 리소스 그룹에 대 한 모든 알림 규칙을 가져옵니다.
*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에 규칙에 대 한 세부 정보가 포함 되어 있지 않습니다.

### 예제 2: 이름으로 알림 규칙 가져오기
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.
*DetailedOutput* 매개 변수가 지정 되지 않았으므로 출력에는 알림 규칙에 대 한 기본 정보만 포함 됩니다.

### 예제 3: 자세한 출력이 있는 이름으로 알림 규칙 가져오기
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

이 명령은 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 라는 경고 규칙을 가져옵니다.
*DetailedOutput* 매개 변수를 지정 하면 출력이 자세히 됩니다.

## 변수

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

### -DetailedOutput
출력에 전체 세부 정보를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
가져올 알림 규칙의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
대상 리소스의 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver 매개 변수

## 출력

### PSAlertRule를 통해 출력 합니다.

## 상속자

## 관련 링크

[추가-AzLogAlertRule](./Add-AzLogAlertRule.md)

[추가-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[추가-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[Get-AzAlertHistory](./Get-AzAlertHistory.md)

[제거-AzAlertRule](./Remove-AzAlertRule.md)


