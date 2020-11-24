---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311435"
---
# <span data-ttu-id="0d5bb-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5bb-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="0d5bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5bb-103">응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="0d5bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d5bb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d5bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d5bb-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5bb-106">**AzApplicationGatewayAutoscaleConfiguration** cmdlet은 기존 응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="0d5bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0d5bb-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5bb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d5bb-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0d5bb-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="0d5bb-110">두 번째 명령은 응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="0d5bb-111">세 번째 명령은 Azure의 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="0d5bb-112">변수</span><span class="sxs-lookup"><span data-stu-id="0d5bb-112">PARAMETERS</span></span>

### <span data-ttu-id="0d5bb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5bb-113">-ApplicationGateway</span></span>
<span data-ttu-id="0d5bb-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5bb-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5bb-115">-DefaultProfile</span></span>
<span data-ttu-id="0d5bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d5bb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0d5bb-117">-Force</span></span>
<span data-ttu-id="0d5bb-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0d5bb-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0d5bb-119">-Confirm</span></span>
<span data-ttu-id="0d5bb-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d5bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5bb-121">-WhatIf</span></span>
<span data-ttu-id="0d5bb-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d5bb-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d5bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5bb-124">CommonParameters</span></span>
<span data-ttu-id="0d5bb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5bb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5bb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5bb-127">입력</span><span class="sxs-lookup"><span data-stu-id="0d5bb-127">INPUTS</span></span>

### <span data-ttu-id="0d5bb-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5bb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d5bb-129">출력</span><span class="sxs-lookup"><span data-stu-id="0d5bb-129">OUTPUTS</span></span>

### <span data-ttu-id="0d5bb-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d5bb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d5bb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0d5bb-131">NOTES</span></span>

## <span data-ttu-id="0d5bb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d5bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d5bb-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5bb-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="0d5bb-134">새로운 AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5bb-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="0d5bb-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5bb-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)