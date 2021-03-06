---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033755"
---
# New-AzVmssIpConfig

## SYNOPSIS
VMSS의 네트워크 인터페이스에 대 한 IP 구성을 만듭니다.

## 구문과

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzVmssIpConfig** CMDLET은 Vmss (가상 컴퓨터 확장 집합)의 네트워크 인터페이스에 대 한 IP 구성 개체를 만듭니다.
이 cmdlet의 구성을 Add-AzVmssNetworkInterfaceConfiguration cmdlet의 *IPConfiguration* 매개 변수로 지정 합니다.

## 예제의

### 예제 1: VMSS 인터페이스에 대 한 IP 구성 개체 만들기
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

이 명령은 ContosoVmssInterface02 이라는 IP 구성 개체를 만듭니다.
이 명령은 $SubnetId에 저장 되어 있는 이전에 정의 된 서브넷 ID를 사용 합니다.
명령은 나중에 **AzVmssNetworkInterfaceConfiguration 추가** 를 사용 하기 위해 $IPConfiguration 변수에 구성 설정을 저장 합니다.

### 예제 2: NAT 풀 설정을 포함 하는 IP 구성 개체 만들기
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

이 명령은 ContosoVmssInterface03 이라는 IP 구성 개체를 만든 다음 나중에 사용 하기 위해이를 $IPConfiguration 변수에 저장 합니다.
이 명령은 $SubnetId에 저장 되어 있는 이전에 정의 된 서브넷 ID를 사용 합니다.
명령은 나중에 사용 하기 위해 $IPConfiguration 변수의 구성 설정을 저장 합니다.
명령에서 *LoadBalancerInboundNatPoolsId* 및 *LoadBalancerBackendAddressPoolsId* 매개 변수에 대 한 값을 지정 합니다.

## 변수

### -ApplicationGatewayBackendAddressPoolsId
부하 분산 장치의 백 엔드 주소 풀에 대 한 참조 배열을 지정 합니다.
확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 백엔드 주소 풀을 참조할 수 있습니다.
여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -DnsSetting
PublicIP 주소에 적용 되는 dns 설정입니다.
PublicIP 주소에 적용 될 Dns 설정의 도메인 이름 레이블
도메인 이름 레이블과 vm 인덱스의 연결은 만들 공용 IP 주소 리소스의 도메인 이름 레이블이 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Ip 태그 개체의 배열을 지정 합니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
부하 분산 장치의 들어오는 NAT (network address translation) 풀에 대 한 참조 배열을 지정 합니다.
확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 들어오는 NAT 풀을 참조할 수 있습니다.
여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
부하 분산 장치의 들어오는 NAT 풀에 대 한 참조 배열을 지정 합니다.
확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 들어오는 NAT 풀을 참조할 수 있습니다.
여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
IP 구성의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -기본
네트워크 인터페이스에 둘 이상의 IP 구성이 있는 경우 기본 IP 구성을 지정 합니다.

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

### -PrivateIPAddressVersion
개인 IP 주소에 대 한 IP 구성을 지정 합니다.  기본값은 IPv4로 간주 됩니다.  사용할 수 있는 값은 ' IPv4 ' 및 ' IPv6 '입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
공용 IP 주소의 유휴 시간 제한

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
PublicIP 주소 구성 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
공용 IP 주소에 대 한 IP 구성을 지정 합니다.  기본값은 IPv4로 간주 됩니다.  사용할 수 있는 값은 ' IPv4 ' 및 ' IPv6 '입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPPrefix
공용 IP 접두사의 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
구성에서 VMSS 네트워크 인터페이스를 만드는 서브넷 ID를 지정 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

### System. 문자열

### System.webserver []

### 시스템. i i.

### Microsoft VirtualMachineScaleSetIpTag []을 (를)

## 출력

### VirtualMachineScaleSetIPConfiguration를 통해 계산 합니다.

## 상속자

## 관련 링크

[추가-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


