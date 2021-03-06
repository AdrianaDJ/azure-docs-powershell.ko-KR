---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: fbfa70146a5eb70d118e6cd1859f968c576d8a0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882961"
---
# Get-AzureRmLoadBalancerInboundNatRuleConfig

## SYNOPSIS
부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 하나 이상의 인바운드 NAT (network address translation) 규칙을 가져옵니다.

## 예제의

### 예제 1: 인바운드 NAT 규칙 구성 가져오기
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고이를 변수 $slb에 저장 합니다.

두 번째 명령은 $slb의 부하 분산 장치에서 MyInboundNatRule1 라는 연결 된 NAT 규칙을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -LoadBalancer
가져올 인바운드 NAT 규칙 구성과 연결 된 부하 분산 장치를 지정 합니다.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
가져올 인바운드 NAT 규칙 구성의 이름을 지정 합니다.

```yaml
Type: String
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

### PSLoadBalancer
' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.

## 출력

### PSInboundNatRule에 대 한.

## 상속자

## 관련 링크

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[새로운 AzureRmLoadBalancerInboundNatRuleConfig](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[제거-AzureRmLoadBalancerInboundNatRuleConfig](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[Set-AzureRmLoadBalancerInboundNatRuleConfig](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


