---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309522"
---
# <span data-ttu-id="626f4-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="626f4-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="626f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="626f4-102">SYNOPSIS</span></span>
<span data-ttu-id="626f4-103">Azure SecurityPartnerProvider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="626f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="626f4-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="626f4-105">DESCRIPTION</span></span>
<span data-ttu-id="626f4-106">**AzSecurityPartnerProvider** Cmdlet은 Azure SecurityPartnerProvider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="626f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="626f4-107">EXAMPLES</span></span>

### <span data-ttu-id="626f4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="626f4-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="626f4-109">변수</span><span class="sxs-lookup"><span data-stu-id="626f4-109">PARAMETERS</span></span>

### <span data-ttu-id="626f4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="626f4-110">-AsJob</span></span>
<span data-ttu-id="626f4-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="626f4-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="626f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626f4-112">-DefaultProfile</span></span>
<span data-ttu-id="626f4-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="626f4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="626f4-114">-Force</span></span>
<span data-ttu-id="626f4-115">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="626f4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="626f4-116">-위치</span><span class="sxs-lookup"><span data-stu-id="626f4-116">-Location</span></span>
<span data-ttu-id="626f4-117">location.</span><span class="sxs-lookup"><span data-stu-id="626f4-117">location.</span></span>

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

### <span data-ttu-id="626f4-118">-이름</span><span class="sxs-lookup"><span data-stu-id="626f4-118">-Name</span></span>
<span data-ttu-id="626f4-119">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="626f4-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626f4-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="626f4-122">-SecurityProviderName</span></span>
<span data-ttu-id="626f4-123">보안 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="626f4-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626f4-124">태그</span><span class="sxs-lookup"><span data-stu-id="626f4-124">-Tag</span></span>
<span data-ttu-id="626f4-125">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="626f4-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="626f4-126">-VirtualHub</span></span>
<span data-ttu-id="626f4-127">보안 파트너 공급자가 연결 된 가상 허브 Id</span><span class="sxs-lookup"><span data-stu-id="626f4-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="626f4-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="626f4-128">-VirtualHubId</span></span>
<span data-ttu-id="626f4-129">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="626f4-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="626f4-130">-VirtualHubName</span></span>
<span data-ttu-id="626f4-131">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="626f4-132">-확인</span><span class="sxs-lookup"><span data-stu-id="626f4-132">-Confirm</span></span>
<span data-ttu-id="626f4-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626f4-134">-WhatIf</span></span>
<span data-ttu-id="626f4-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="626f4-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626f4-137">CommonParameters</span></span>
<span data-ttu-id="626f4-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="626f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626f4-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="626f4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626f4-140">입력</span><span class="sxs-lookup"><span data-stu-id="626f4-140">INPUTS</span></span>

### <span data-ttu-id="626f4-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="626f4-141">System.String</span></span>

### <span data-ttu-id="626f4-142">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="626f4-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="626f4-143">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="626f4-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="626f4-144">출력</span><span class="sxs-lookup"><span data-stu-id="626f4-144">OUTPUTS</span></span>

### <span data-ttu-id="626f4-145">PSSecurityPartnerProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="626f4-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="626f4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="626f4-146">NOTES</span></span>

## <span data-ttu-id="626f4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="626f4-147">RELATED LINKS</span></span>