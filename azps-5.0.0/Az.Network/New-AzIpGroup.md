---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309581"
---
# <span data-ttu-id="e3602-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3602-101">New-AzIpGroup</span></span>

## <span data-ttu-id="e3602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3602-102">SYNOPSIS</span></span>
<span data-ttu-id="e3602-103">Azure IpGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="e3602-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3602-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3602-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3602-105">DESCRIPTION</span></span>
<span data-ttu-id="e3602-106">**AzIpGroup** Cmdlet은 Azure ipgroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="e3602-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e3602-107">EXAMPLES</span></span>

### <span data-ttu-id="e3602-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3602-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="e3602-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3602-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="e3602-110">변수</span><span class="sxs-lookup"><span data-stu-id="e3602-110">PARAMETERS</span></span>

### <span data-ttu-id="e3602-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3602-111">-AsJob</span></span>
<span data-ttu-id="e3602-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3602-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3602-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3602-113">-DefaultProfile</span></span>
<span data-ttu-id="e3602-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3602-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e3602-115">-Force</span></span>
<span data-ttu-id="e3602-116">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e3602-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3602-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e3602-117">-IpAddress</span></span>
<span data-ttu-id="e3602-118">IpGroup에 정의 된 IpAddresses</span><span class="sxs-lookup"><span data-stu-id="e3602-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3602-119">-위치</span><span class="sxs-lookup"><span data-stu-id="e3602-119">-Location</span></span>
<span data-ttu-id="e3602-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-120">The location.</span></span>

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

### <span data-ttu-id="e3602-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e3602-121">-Name</span></span>
<span data-ttu-id="e3602-122">Ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="e3602-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3602-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3602-124">Ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="e3602-125">태그</span><span class="sxs-lookup"><span data-stu-id="e3602-125">-Tag</span></span>
<span data-ttu-id="e3602-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e3602-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e3602-127">-Confirm</span></span>
<span data-ttu-id="e3602-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3602-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3602-129">-WhatIf</span></span>
<span data-ttu-id="e3602-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3602-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3602-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3602-132">CommonParameters</span></span>
<span data-ttu-id="e3602-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3602-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3602-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3602-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3602-135">입력</span><span class="sxs-lookup"><span data-stu-id="e3602-135">INPUTS</span></span>

### <span data-ttu-id="e3602-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3602-136">System.String</span></span>

### <span data-ttu-id="e3602-137">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e3602-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="e3602-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e3602-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3602-139">출력</span><span class="sxs-lookup"><span data-stu-id="e3602-139">OUTPUTS</span></span>

### <span data-ttu-id="e3602-140">PSIpGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e3602-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="e3602-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e3602-141">NOTES</span></span>

## <span data-ttu-id="e3602-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3602-142">RELATED LINKS</span></span>