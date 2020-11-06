---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534267"
---
# <span data-ttu-id="d027e-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d027e-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="d027e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d027e-102">SYNOPSIS</span></span>
<span data-ttu-id="d027e-103">부하 분산 장치에 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d027e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d027e-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d027e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d027e-105">DESCRIPTION</span></span>
<span data-ttu-id="d027e-106">**Add-AzureRmLoadBalancerProbeConfig** Cmdlet은 Azure 부하 분산 장치에 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d027e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d027e-107">EXAMPLES</span></span>

### <span data-ttu-id="d027e-108">예제 1 부하 분산 장치에 프로브 구성 추가</span><span class="sxs-lookup"><span data-stu-id="d027e-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d027e-109">이 명령은 myLb 라는 로드 균형 조정기를 가져와 지정 된 프로브 구성을이에 추가한 다음 **AzureRmLoadBalancer** cmdlet을 사용 하 여 부하 분산 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="d027e-110">변수</span><span class="sxs-lookup"><span data-stu-id="d027e-110">PARAMETERS</span></span>

### <span data-ttu-id="d027e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d027e-111">-DefaultProfile</span></span>
<span data-ttu-id="d027e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d027e-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d027e-113">-IntervalInSeconds</span></span>
<span data-ttu-id="d027e-114">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d027e-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d027e-115">-LoadBalancer</span></span>
<span data-ttu-id="d027e-116">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d027e-117">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d027e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d027e-118">-Name</span></span>
<span data-ttu-id="d027e-119">추가할 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-119">Specifies the name of the probe configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d027e-120">-포트</span><span class="sxs-lookup"><span data-stu-id="d027e-120">-Port</span></span>
<span data-ttu-id="d027e-121">프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d027e-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="d027e-122">-ProbeCount</span></span>
<span data-ttu-id="d027e-123">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d027e-124">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="d027e-124">-Protocol</span></span>
<span data-ttu-id="d027e-125">프로브에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="d027e-126">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="d027e-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="d027e-127">-RequestPath</span></span>
<span data-ttu-id="d027e-128">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="d027e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d027e-129">-Confirm</span></span>
<span data-ttu-id="d027e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d027e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d027e-131">-WhatIf</span></span>
<span data-ttu-id="d027e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d027e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d027e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d027e-134">CommonParameters</span></span>
<span data-ttu-id="d027e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d027e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d027e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d027e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d027e-137">입력</span><span class="sxs-lookup"><span data-stu-id="d027e-137">INPUTS</span></span>

### <span data-ttu-id="d027e-138">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d027e-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="d027e-139">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d027e-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="d027e-140">출력</span><span class="sxs-lookup"><span data-stu-id="d027e-140">OUTPUTS</span></span>

### <span data-ttu-id="d027e-141">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d027e-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d027e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d027e-142">NOTES</span></span>

## <span data-ttu-id="d027e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d027e-143">RELATED LINKS</span></span>

[<span data-ttu-id="d027e-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d027e-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="d027e-145">새로운 AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d027e-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="d027e-146">제거-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d027e-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="d027e-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d027e-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="d027e-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d027e-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

