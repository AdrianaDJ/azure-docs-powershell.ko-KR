---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308105"
---
# <span data-ttu-id="e910a-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-101">Remove-AzVM</span></span>

## <span data-ttu-id="e910a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e910a-102">SYNOPSIS</span></span>
<span data-ttu-id="e910a-103">Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="e910a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e910a-104">SYNTAX</span></span>

### <span data-ttu-id="e910a-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e910a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e910a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e910a-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e910a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e910a-107">DESCRIPTION</span></span>
<span data-ttu-id="e910a-108">**AzVM** Cmdlet은 Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="e910a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e910a-109">EXAMPLES</span></span>

### <span data-ttu-id="e910a-110">예제 1: 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="e910a-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e910a-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="e910a-112">변수</span><span class="sxs-lookup"><span data-stu-id="e910a-112">PARAMETERS</span></span>

### <span data-ttu-id="e910a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e910a-113">-AsJob</span></span>
<span data-ttu-id="e910a-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e910a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e910a-115">-DefaultProfile</span></span>
<span data-ttu-id="e910a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e910a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e910a-117">-Force</span></span>
<span data-ttu-id="e910a-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e910a-119">-Id</span><span class="sxs-lookup"><span data-stu-id="e910a-119">-Id</span></span>
<span data-ttu-id="e910a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e910a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e910a-121">-Name</span></span>
<span data-ttu-id="e910a-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e910a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e910a-123">-NoWait</span></span>
<span data-ttu-id="e910a-124">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e910a-125">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e910a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e910a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e910a-127">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e910a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e910a-128">-Confirm</span></span>
<span data-ttu-id="e910a-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e910a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e910a-130">-WhatIf</span></span>
<span data-ttu-id="e910a-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e910a-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e910a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e910a-133">CommonParameters</span></span>
<span data-ttu-id="e910a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e910a-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e910a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e910a-136">입력</span><span class="sxs-lookup"><span data-stu-id="e910a-136">INPUTS</span></span>

### <span data-ttu-id="e910a-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e910a-137">System.String</span></span>

## <span data-ttu-id="e910a-138">출력</span><span class="sxs-lookup"><span data-stu-id="e910a-138">OUTPUTS</span></span>

### <span data-ttu-id="e910a-139">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="e910a-140">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e910a-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e910a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e910a-141">NOTES</span></span>

## <span data-ttu-id="e910a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e910a-142">RELATED LINKS</span></span>

[<span data-ttu-id="e910a-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e910a-144">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e910a-145">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e910a-146">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e910a-147">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e910a-148">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="e910a-148">Update-AzVM</span></span>](./Update-AzVM.md)

