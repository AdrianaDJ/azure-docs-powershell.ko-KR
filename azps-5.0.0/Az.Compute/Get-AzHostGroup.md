---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310367"
---
# <span data-ttu-id="c7689-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="c7689-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="c7689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7689-102">SYNOPSIS</span></span>
<span data-ttu-id="c7689-103">호스트를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-103">Get or list hosts.</span></span>

## <span data-ttu-id="c7689-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7689-104">SYNTAX</span></span>

### <span data-ttu-id="c7689-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7689-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7689-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c7689-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7689-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c7689-107">DESCRIPTION</span></span>
<span data-ttu-id="c7689-108">이 cmdlet은 호스트 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="c7689-109">또한이 cmdlet은 호스트 그룹 이름이 지정 되지 않은 경우 리소스 그룹의 모든 호스트 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="c7689-110">또한이 cmdlet은 호스트 그룹 이름 또는 리소스 그룹 이름이 없는 경우 구독에 모든 호스트 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="c7689-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c7689-111">EXAMPLES</span></span>

### <span data-ttu-id="c7689-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7689-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="c7689-113">이 명령은 호스트 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-113">This command returns a host group.</span></span>

### <span data-ttu-id="c7689-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7689-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="c7689-115">이 명령은 지정 된 리소스 그룹의 모든 호스트 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="c7689-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="c7689-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="c7689-117">이 명령은 구독에 있는 모든 호스트 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="c7689-118">변수</span><span class="sxs-lookup"><span data-stu-id="c7689-118">PARAMETERS</span></span>

### <span data-ttu-id="c7689-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7689-119">-DefaultProfile</span></span>
<span data-ttu-id="c7689-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7689-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="c7689-121">-InstanceView</span></span>
<span data-ttu-id="c7689-122">반환 된 개체를 확장 하 여 호스트의 인스턴스 뷰도 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7689-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c7689-123">-Name</span></span>
<span data-ttu-id="c7689-124">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7689-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7689-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7689-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7689-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7689-127">-ResourceId</span></span>
<span data-ttu-id="c7689-128">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7689-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7689-129">CommonParameters</span></span>
<span data-ttu-id="c7689-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7689-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7689-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7689-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7689-132">입력</span><span class="sxs-lookup"><span data-stu-id="c7689-132">INPUTS</span></span>

### <span data-ttu-id="c7689-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7689-133">System.String</span></span>

## <span data-ttu-id="c7689-134">출력</span><span class="sxs-lookup"><span data-stu-id="c7689-134">OUTPUTS</span></span>

### <span data-ttu-id="c7689-135">PSHostGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="c7689-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="c7689-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c7689-136">NOTES</span></span>

## <span data-ttu-id="c7689-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7689-137">RELATED LINKS</span></span>