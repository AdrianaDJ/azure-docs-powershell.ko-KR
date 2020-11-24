---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308411"
---
# <span data-ttu-id="e3e6a-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e3e6a-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="e3e6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e6a-102">SYNOPSIS</span></span> 
<span data-ttu-id="e3e6a-103">Vpn 클라이언트 연결당 Azure 가상 네트워크 게이트웨이의 vpn 클라이언트 연결 상태 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3e6a-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="e3e6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3e6a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="e3e6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="e3e6a-106">연결 된 모든 vpn 클라이언트 연결 상태를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e6a-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="e3e6a-107">여기에는 vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3e6a-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="e3e6a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e3e6a-108">EXAMPLES</span></span>

### <span data-ttu-id="e3e6a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3e6a-109">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="e3e6a-110">리소스 그룹 리소스 그룹과 같은 Azure 가상 네트워크 게이트웨이의 경우 OpenVpn을 사용 하 여 현재 연결 된 vpn 클라이언트 연결을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e6a-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="e3e6a-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3e6a-111">Example 2</span></span>

<span data-ttu-id="e3e6a-112">Vpn 클라이언트 연결당 Azure 가상 네트워크 게이트웨이의 vpn 클라이언트 연결 상태 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3e6a-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="e3e6a-113">생성</span><span class="sxs-lookup"><span data-stu-id="e3e6a-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="e3e6a-114">변수</span><span class="sxs-lookup"><span data-stu-id="e3e6a-114">PARAMETERS</span></span>

### <span data-ttu-id="e3e6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3e6a-116">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e3e6a-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="e3e6a-117">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="e3e6a-117">-ResourceName</span></span>
<span data-ttu-id="e3e6a-118">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="e3e6a-118">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="e3e6a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e6a-119">-ResourceId</span></span>
<span data-ttu-id="e3e6a-120">가상 네트워크 게이트웨이 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e3e6a-120">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e6a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3e6a-121">-InputObject</span></span>
<span data-ttu-id="e3e6a-122">가상 네트워크 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="e3e6a-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e6a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3e6a-123">-AsJob</span></span>
<span data-ttu-id="e3e6a-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3e6a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3e6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e6a-125">CommonParameters</span></span>
<span data-ttu-id="e3e6a-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e6a-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3e6a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e6a-128">입력</span><span class="sxs-lookup"><span data-stu-id="e3e6a-128">INPUTS</span></span>

### <span data-ttu-id="e3e6a-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3e6a-129">System.String</span></span>

## <span data-ttu-id="e3e6a-130">출력</span><span class="sxs-lookup"><span data-stu-id="e3e6a-130">OUTPUTS</span></span>

### <span data-ttu-id="e3e6a-131">Microsoft. Azure. Ps네트워크 경로</span><span class="sxs-lookup"><span data-stu-id="e3e6a-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="e3e6a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e3e6a-132">NOTES</span></span>

## <span data-ttu-id="e3e6a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3e6a-133">RELATED LINKS</span></span>