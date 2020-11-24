---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310148"
---
# <span data-ttu-id="25081-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="25081-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="25081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25081-102">SYNOPSIS</span></span>
<span data-ttu-id="25081-103">수정 된 IpAllocation을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="25081-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="25081-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25081-104">SYNTAX</span></span>

### <span data-ttu-id="25081-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25081-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25081-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25081-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25081-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25081-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25081-108">설명은</span><span class="sxs-lookup"><span data-stu-id="25081-108">DESCRIPTION</span></span>
<span data-ttu-id="25081-109">**AzIpAllocation** Cmdlet은 Azure ip 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25081-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="25081-110">예제의</span><span class="sxs-lookup"><span data-stu-id="25081-110">EXAMPLES</span></span>

### <span data-ttu-id="25081-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="25081-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="25081-112">변수</span><span class="sxs-lookup"><span data-stu-id="25081-112">PARAMETERS</span></span>

### <span data-ttu-id="25081-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25081-113">-AsJob</span></span>
<span data-ttu-id="25081-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="25081-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25081-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25081-115">-DefaultProfile</span></span>
<span data-ttu-id="25081-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25081-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25081-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25081-117">-InputObject</span></span>
<span data-ttu-id="25081-118">IpAllocation</span><span class="sxs-lookup"><span data-stu-id="25081-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25081-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="25081-119">-IpAllocationTag</span></span>
<span data-ttu-id="25081-120">IP 할당의 할당 태그</span><span class="sxs-lookup"><span data-stu-id="25081-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25081-121">-이름</span><span class="sxs-lookup"><span data-stu-id="25081-121">-Name</span></span>
<span data-ttu-id="25081-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25081-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25081-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25081-123">-ResourceGroupName</span></span>
<span data-ttu-id="25081-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25081-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25081-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25081-125">-ResourceId</span></span>
<span data-ttu-id="25081-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="25081-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25081-127">태그</span><span class="sxs-lookup"><span data-stu-id="25081-127">-Tag</span></span>
<span data-ttu-id="25081-128">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="25081-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25081-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25081-129">CommonParameters</span></span>
<span data-ttu-id="25081-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25081-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25081-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25081-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25081-132">입력</span><span class="sxs-lookup"><span data-stu-id="25081-132">INPUTS</span></span>

### <span data-ttu-id="25081-133">PSIpAllocation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="25081-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="25081-134">출력</span><span class="sxs-lookup"><span data-stu-id="25081-134">OUTPUTS</span></span>

### <span data-ttu-id="25081-135">PSIpAllocation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="25081-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="25081-136">상속자</span><span class="sxs-lookup"><span data-stu-id="25081-136">NOTES</span></span>

## <span data-ttu-id="25081-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25081-137">RELATED LINKS</span></span>