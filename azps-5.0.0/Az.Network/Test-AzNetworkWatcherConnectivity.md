---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 8d3a714f2798c4866df39cd63c664228f078c37c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310766"
---
# <span data-ttu-id="217df-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="217df-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="217df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="217df-102">SYNOPSIS</span></span>
<span data-ttu-id="217df-103">지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="217df-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="217df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="217df-104">SYNTAX</span></span>

### <span data-ttu-id="217df-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="217df-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="217df-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="217df-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="217df-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="217df-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="217df-108">설명은</span><span class="sxs-lookup"><span data-stu-id="217df-108">DESCRIPTION</span></span>
<span data-ttu-id="217df-109">Test-AzNetworkWatcherConnectivity cmdlet은 지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="217df-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="217df-110">원본과 대상 간의 연결을 설정할 수 없는 경우 cmdlet은 문제에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="217df-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="217df-111">예제의</span><span class="sxs-lookup"><span data-stu-id="217df-111">EXAMPLES</span></span>

### <span data-ttu-id="217df-112">예제 1: VM에서 웹 사이트로 네트워크 감시자 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="217df-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="217df-113">이 예제에서는 Azure의 VM에서 www.bing.com에 대 한 연결을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="217df-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="217df-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="217df-114">Example 2</span></span>

<span data-ttu-id="217df-115">지정 된 원본 VM 및 대상에 대 한 연결 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="217df-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="217df-116">생성</span><span class="sxs-lookup"><span data-stu-id="217df-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="217df-117">변수</span><span class="sxs-lookup"><span data-stu-id="217df-117">PARAMETERS</span></span>

### <span data-ttu-id="217df-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="217df-118">-AsJob</span></span>
<span data-ttu-id="217df-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="217df-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="217df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217df-120">-DefaultProfile</span></span>
<span data-ttu-id="217df-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="217df-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="217df-122">-DestinationAddress</span></span>
<span data-ttu-id="217df-123">연결을 시도 하는 데 사용할 리소스의 IP 주소 또는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217df-124">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="217df-124">-DestinationId</span></span>
<span data-ttu-id="217df-125">연결 시도가 수행 될 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-125">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217df-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="217df-126">-DestinationPort</span></span>
<span data-ttu-id="217df-127">확인 연결을 수행할 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-127">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217df-128">-위치</span><span class="sxs-lookup"><span data-stu-id="217df-128">-Location</span></span>
<span data-ttu-id="217df-129">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-129">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217df-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="217df-130">-NetworkWatcher</span></span>
<span data-ttu-id="217df-131">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="217df-131">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="217df-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="217df-132">-NetworkWatcherName</span></span>
<span data-ttu-id="217df-133">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217df-134">프로토콜 구성</span><span class="sxs-lookup"><span data-stu-id="217df-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="217df-135">확인 연결을 수행할 프로토콜 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-135">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217df-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217df-136">-ResourceGroupName</span></span>
<span data-ttu-id="217df-137">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-137">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217df-138">-SourceId</span><span class="sxs-lookup"><span data-stu-id="217df-138">-SourceId</span></span>
<span data-ttu-id="217df-139">연결 검사가 시작 되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217df-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="217df-140">-SourcePort</span></span>
<span data-ttu-id="217df-141">연결 검사가 수행 되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="217df-141">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217df-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217df-142">CommonParameters</span></span>
<span data-ttu-id="217df-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="217df-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217df-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217df-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217df-145">입력</span><span class="sxs-lookup"><span data-stu-id="217df-145">INPUTS</span></span>

### <span data-ttu-id="217df-146">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="217df-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="217df-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="217df-147">System.String</span></span>

### <span data-ttu-id="217df-148">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="217df-148">System.Int32</span></span>

## <span data-ttu-id="217df-149">출력</span><span class="sxs-lookup"><span data-stu-id="217df-149">OUTPUTS</span></span>

### <span data-ttu-id="217df-150">PSConnectivityInformation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="217df-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="217df-151">상속자</span><span class="sxs-lookup"><span data-stu-id="217df-151">NOTES</span></span>
<span data-ttu-id="217df-152">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="217df-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="217df-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="217df-153">RELATED LINKS</span></span>

<span data-ttu-id="217df-154">[새로운 AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [제거-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="217df-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="217df-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="217df-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="217df-156">[새로운 AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [새로운 AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [제거-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [중지-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="217df-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="217df-157">[시작-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [새로운 AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [테스트-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [테스트-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [중지-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [시작-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [제거-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [새로운 AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="217df-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>