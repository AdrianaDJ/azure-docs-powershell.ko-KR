---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048393"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
가상 컴퓨터에 대 한 운영 체제 속성을 설정 합니다.

## 구문과

### Windows (기본값)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzVMOperatingSystem** cmdlet은 가상 컴퓨터의 운영 체제 속성을 설정 합니다.
로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.

## 예제의

### 예제 1: 새 가상 컴퓨터의 운영 체제 속성 설정
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

첫 번째 명령은 암호를 안전한 문자열로 변환한 다음 $SecurePassword 변수에 저장 합니다.
자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.
두 번째 명령은 사용자의 자격 증명을 만들고 $SecurePassword에 저장 된 암호를 만든 다음 $Credential 변수에 자격 증명을 저장 합니다.
자세한 내용은을 입력 `Get-Help New-Object` 하세요.
세 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.
네 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.
가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.
다음 네 개의 명령은 다음 명령에 사용할 변수에 값을 할당 합니다.
이러한 문자열은 **Set-AzVMOperatingSystem** 명령에서 직접 지정할 수 있으므로이 접근 방식은 가독성을 위해 사용 됩니다.
그러나이 방법을 스크립트에 사용할 수 있습니다.
마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터의 운영 체제 속성을 설정 합니다.
이 명령은 $Credential에 저장 된 자격 증명을 사용 합니다.
명령에서는 일부 매개 변수에 대해 이전 명령에서 할당 된 변수를 사용 합니다.

## 변수

### -ComputerName
컴퓨터의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
가상 컴퓨터에 대 한 사용자 이름 및 암호를 **PSCredential** 개체로 지정 합니다.
자격 증명을 얻으려면 Get-Credential cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.
이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.
이진 배열의 최대 길이는 65535 바이트입니다.<br>
**참고: customData 속성에서 비밀 번호 또는 암호를 전달 하지 마세요.**<br>
VM을 만든 후에는이 속성을 업데이트할 수 없습니다. <br>
customData가 파일로 저장 되도록 VM에 전달 됩니다. 자세한 내용은 [Azure vm의 사용자 지정 데이터](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) 를 참조 하세요. <br>
Linux VM에 대 한 클라우드 초기화를 사용 [하려면 클라우드 초기화를 사용 하 여 LINUX vm을 만드는 동안 사용자 지정](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) 을 참조 하세요.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -DisablePasswordAuthentication
이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
VM 에이전트 프로 비전을 사용 하지 않도록 설정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate 업데이트
이 cmdlet이 자동 업데이트를 사용할 수 있음을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
운영 체제 유형이 Linux 임을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
IaaS 가상 컴퓨터에 대 한 게스트의 실시간 패치 모드를 지정 합니다.<br><br>
사용할 수 있는 값은 다음과 같습니다.<br>
**수동** -가상 컴퓨터에 대 한 패치 적용을 제어 합니다. VM 내에서 수동으로 패치를 적용 하 여이 작업을 수행 합니다. 이 모드에서는 자동 업데이트를 사용할 수 없습니다. WindowsConfiguration는 속성을 설정 합니다. Enable자동 업데이트는 false 여야 합니다.<br>
자동 **으로 os가** 가상 컴퓨터를 업데이트 합니다. 이 속성은 WindowsConfiguration입니다. Enable자동 업데이트는 true 여야 합니다. <br >
자동 **Byplatform** -가상 머신은 OS에 의해 자동으로 업데이트 됩니다. ProvisionVMAgent 및 WindowsConfiguration 속성은 true이 고 반드시 업데이트 해야 합니다.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
설정에 따라 가상 컴퓨터에 가상 컴퓨터 에이전트가 설치 되어 있어야 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -표준 시간대
가상 컴퓨터의 표준 시간대를 지정 합니다. 예: \" 태평양 표준시 시간 \" . <br>
가능한 값은 [TimeZoneInfo Systemtimezones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)에서 반환 된 표준 시간대의 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 값이 될 수 있습니다.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
운영 체제 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.
New-AzVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
운영 체제 유형이 Windows 임을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
WinRM 인증서의 URI를 지정 합니다.
이를 키 보관소에 저장 해야 합니다.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
이 운영 체제에서 HTTP WinRM을 사용 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
이 운영 체제에서 HTTPS WinRM을 사용 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### PSVirtualMachine를 계산 합니다.

### System.webserver 매개 변수

### System. 문자열

### System.webserver. PSCredential

### 시스템 Uri

## 출력

### PSVirtualMachine를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[새로운 AzVMConfig](./New-AzVMConfig.md)

