---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876579"
---
# Set-AzLoadBalancerInboundNatRuleConfig

## SYNOPSIS
부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.

## 구문과

### SetByResourceId
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResource
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 NAT (network address translation) 규칙 구성을 설정 합니다.

## 예제의

### 예제 1: 부하 분산 장치에서 인바운드 NAT 규칙 구성 수정
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.

두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산 장치를 Add-AzLoadBalancerInboundNatRuleConfig에 전달 하 여 인바운드 NAT 규칙 구성을 추가 합니다.

세 번째 명령은 인바운드 NAT 규칙 구성을 저장 하 고 업데이트 하는 부하 분산을 **설정-AzLoadBalancerInboundNatRuleConfig** 에 전달 합니다.
이전 명령에서 사용 하도록 설정 된 부동 IP를 사용 하지 않고 규칙 구성이 설정 되어 있는지 확인 합니다.

## 변수

### -BackendPort
이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.

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

### -EnableFloatingIP
이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.

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

### -FrontendIpConfiguration
인바운드 NAT 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendIpConfigurationId
프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPort
부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.

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

### -IdleTimeoutInMinutes
부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.

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

### -LoadBalancer
부하 분산 장치를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 설정 합니다.

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
인바운드 NAT 규칙 구성의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로토콜
인바운드 NAT 규칙 구성으로 일치 하는 프로토콜을 지정 합니다.
이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSLoadBalancer
' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. 네트워크. PSLoadBalancer

## 상속자

## 관련 링크

[추가-AzLoadBalancerInboundNatRuleConfig](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Get-AzLoadBalancerInboundNatRuleConfig](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[새로운 AzLoadBalancerInboundNatRuleConfig](./New-AzLoadBalancerInboundNatRuleConfig.md)

[제거-AzLoadBalancerInboundNatRuleConfig](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


