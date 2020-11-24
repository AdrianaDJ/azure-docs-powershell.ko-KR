---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 981cef591aab936e07c2a9b07b360390491403c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304208"
---
# <span data-ttu-id="8d6c0-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="8d6c0-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="8d6c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6c0-103">VMSS 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="8d6c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d6c0-104">SYNTAX</span></span>

### <span data-ttu-id="8d6c0-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d6c0-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d6c0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8d6c0-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d6c0-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8d6c0-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d6c0-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8d6c0-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d6c0-109">SimulateEvictionMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8d6c0-109">SimulateEvictionMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d6c0-110">설명은</span><span class="sxs-lookup"><span data-stu-id="8d6c0-110">DESCRIPTION</span></span>
<span data-ttu-id="8d6c0-111">**AzVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-111">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8d6c0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8d6c0-112">EXAMPLES</span></span>

### <span data-ttu-id="8d6c0-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d6c0-113">Example 1</span></span>

<span data-ttu-id="8d6c0-114">VMSS 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-114">Modifies the state of a VMSS instance.</span></span> <span data-ttu-id="8d6c0-115">생성</span><span class="sxs-lookup"><span data-stu-id="8d6c0-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVmssVM -InstanceId <String> -Reimage -ResourceGroupName myresourcegroup -VMScaleSetName 'VMSS001'
```

## <span data-ttu-id="8d6c0-116">변수</span><span class="sxs-lookup"><span data-stu-id="8d6c0-116">PARAMETERS</span></span>

### <span data-ttu-id="8d6c0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d6c0-117">-AsJob</span></span>
<span data-ttu-id="8d6c0-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8d6c0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d6c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6c0-119">-DefaultProfile</span></span>
<span data-ttu-id="8d6c0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d6c0-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8d6c0-121">-InstanceId</span></span>
<span data-ttu-id="8d6c0-122">이 cmdlet에서 상태를 수정 하는 VMSS 인스턴스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-122">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="8d6c0-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="8d6c0-123">-PerformMaintenance</span></span>
<span data-ttu-id="8d6c0-124">이 cmdlet이 VMSS의 가상 컴퓨터에서 유지 관리를 수행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-124">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-125">-재배포</span><span class="sxs-lookup"><span data-stu-id="8d6c0-125">-Redeploy</span></span>
<span data-ttu-id="8d6c0-126">이 cmdlet이 VMSS에서 가상 컴퓨터를 다시 배포 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-126">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-127">-이미지로</span><span class="sxs-lookup"><span data-stu-id="8d6c0-127">-Reimage</span></span>
<span data-ttu-id="8d6c0-128">이 cmdlet이 VMSS 인스턴스를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-128">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-129">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="8d6c0-129">-ReimageAll</span></span>
<span data-ttu-id="8d6c0-130">Cmdlet이 VMSS 인스턴스의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-130">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d6c0-131">-ResourceGroupName</span></span>
<span data-ttu-id="8d6c0-132">VMSS 인스턴스가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-132">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-133">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="8d6c0-133">-SimulateEviction</span></span>
<span data-ttu-id="8d6c0-134">이 cmdlet이 VM 배율 집합에서 스폿 가상 컴퓨터의 제거를 시뮬레이션 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-134">Indicates that this cmdlet simulates the eviction of spot virtual machine in a VM scale set.</span></span>
<span data-ttu-id="8d6c0-135">제거는 API를 호출 하는 30 분 내에 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-135">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8d6c0-136">-VMScaleSetName</span></span>
<span data-ttu-id="8d6c0-137">이 cmdlet이 수정 하는 VMSS 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-137">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c0-138">-확인</span><span class="sxs-lookup"><span data-stu-id="8d6c0-138">-Confirm</span></span>
<span data-ttu-id="8d6c0-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d6c0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d6c0-140">-WhatIf</span></span>
<span data-ttu-id="8d6c0-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d6c0-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d6c0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6c0-143">CommonParameters</span></span>
<span data-ttu-id="8d6c0-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6c0-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6c0-146">입력</span><span class="sxs-lookup"><span data-stu-id="8d6c0-146">INPUTS</span></span>

### <span data-ttu-id="8d6c0-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d6c0-147">System.String</span></span>

## <span data-ttu-id="8d6c0-148">출력</span><span class="sxs-lookup"><span data-stu-id="8d6c0-148">OUTPUTS</span></span>

### <span data-ttu-id="8d6c0-149">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="8d6c0-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8d6c0-150">상속자</span><span class="sxs-lookup"><span data-stu-id="8d6c0-150">NOTES</span></span>

## <span data-ttu-id="8d6c0-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d6c0-151">RELATED LINKS</span></span>

[<span data-ttu-id="8d6c0-152">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="8d6c0-152">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)