---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216060"
---
# Get-AzNotificationHub

## SYNOPSIS
알림 허브에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNotificationHub** cmdlet은 지정 된 네임 스페이스의 notification hubs에 대 한 정보를 가져오고 지정 된 리소스 그룹에 할당 합니다.
예를 들어 네임 스페이스 ContosoNamespace의 모든 알림 허브에 대 한 정보를 가져오고 ContosoNotificationsGroup 리소스 그룹에 할당할 수 있습니다.
또는 *Notificationhub* 매개 변수를 사용 하 여 반환 된 데이터를 특정 알림 허브에 대 한 정보로 제한할 수 있습니다.
알림 허브는 해당 클라이언트에서 사용 하는 iOS, Android, Windows Phone 8, Windows 스토어 등의 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.
이러한 허브는 개별 앱과 거의 동일 하며 각 앱에는 일반적으로 자체 알림 허브가 있습니다.
이 cmdlet은 허브 자체에 대 한 정보만 가져옵니다.
AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys 및 Get-AzNotificationHubPNSCredentials 등의 다른 cmdlet은 허브의 권한 부여 규칙, 연결 문자열 및 플랫폼 알림 서비스 자격 증명에 대 한 정보를 가져오기 위해 필요 합니다.

## 예제의

### 예제 1: 특정 네임 스페이스의 모든 알림 허브에 대 한 정보 가져오기
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당 된 ContosoNamespace 이라는 네임 스페이스에 있는 모든 알림 허브에 대 한 정보를 가져옵니다.

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

### -Namespace
알림 허브가 할당 된 네임 스페이스를 지정 합니다.
네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.

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

### -NotificationHub
이 cmdlet이 가져오는 알림 허브의 이름을 지정 합니다.
알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
알림 허브가 할당 된 리소스 그룹을 지정 합니다.
리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure. NotificationHubAttributes

## 상속자

## 관련 링크

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Get-AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[Get-AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[새로운 AzNotificationHub](./New-AzNotificationHub.md)

[제거-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


