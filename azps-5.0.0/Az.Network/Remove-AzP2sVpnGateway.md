---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311399"
---
# <span data-ttu-id="1613c-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1613c-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="1613c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1613c-102">SYNOPSIS</span></span>
<span data-ttu-id="1613c-103">기존 P2SVpnGateway를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="1613c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1613c-104">SYNTAX</span></span>

### <span data-ttu-id="1613c-105">ByP2SVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1613c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1613c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1613c-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1613c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="1613c-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1613c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1613c-108">DESCRIPTION</span></span>
<span data-ttu-id="1613c-109">**AzP2sVpnGateway** cmdlet을 사용 하면 virtualhub에서 기존 P2SVpnGateway를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="1613c-110">P2SVpnGateway가 제거 된 후에는 사이트 클라이언트 연결에 대 한 모든 지점이 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="1613c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1613c-111">EXAMPLES</span></span>

### <span data-ttu-id="1613c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1613c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="1613c-113">**AzP2sVpnGateway** cmdlet을 사용 하면 virtualhub에서 기존 P2SVpnGateway를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="1613c-114">변수</span><span class="sxs-lookup"><span data-stu-id="1613c-114">PARAMETERS</span></span>

### <span data-ttu-id="1613c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1613c-115">-DefaultProfile</span></span>
<span data-ttu-id="1613c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1613c-117">-Force</span></span>
<span data-ttu-id="1613c-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1613c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1613c-119">-InputObject</span></span>
<span data-ttu-id="1613c-120">삭제할 p2sVpnGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1613c-121">-Name</span></span>
<span data-ttu-id="1613c-122">P2SVpnGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1613c-123">-PassThru</span></span>
<span data-ttu-id="1613c-124">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="1613c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1613c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1613c-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1613c-127">-ResourceId</span></span>
<span data-ttu-id="1613c-128">삭제할 p2sVpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1613c-129">-Confirm</span></span>
<span data-ttu-id="1613c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1613c-131">-WhatIf</span></span>
<span data-ttu-id="1613c-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1613c-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1613c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1613c-134">CommonParameters</span></span>
<span data-ttu-id="1613c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1613c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1613c-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1613c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1613c-137">입력</span><span class="sxs-lookup"><span data-stu-id="1613c-137">INPUTS</span></span>

### <span data-ttu-id="1613c-138">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1613c-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="1613c-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1613c-139">System.String</span></span>

## <span data-ttu-id="1613c-140">출력</span><span class="sxs-lookup"><span data-stu-id="1613c-140">OUTPUTS</span></span>

### <span data-ttu-id="1613c-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1613c-141">System.Boolean</span></span>

## <span data-ttu-id="1613c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1613c-142">NOTES</span></span>

## <span data-ttu-id="1613c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1613c-143">RELATED LINKS</span></span>