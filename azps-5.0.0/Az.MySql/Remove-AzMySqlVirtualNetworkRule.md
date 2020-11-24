---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 85690d3602744f6bde45a5f08b5a927124a8460a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304526"
---
# <span data-ttu-id="80ee1-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="80ee1-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="80ee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="80ee1-103">지정 된 이름의 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="80ee1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80ee1-104">SYNTAX</span></span>

### <span data-ttu-id="80ee1-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="80ee1-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="80ee1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80ee1-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80ee1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="80ee1-107">DESCRIPTION</span></span>
<span data-ttu-id="80ee1-108">지정 된 이름의 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="80ee1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="80ee1-109">EXAMPLES</span></span>

### <span data-ttu-id="80ee1-110">예제 1: 이름별로 MySql 서버 가상 네트워크 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="80ee1-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="80ee1-111">이 cmdlet은 이름으로 MySql 서버 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="80ee1-112">예제 2: id 별 MySql 서버 가상 네트워크 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="80ee1-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="80ee1-113">이러한 cmdlet은 id를 기준으로 MySql 서버 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="80ee1-114">변수</span><span class="sxs-lookup"><span data-stu-id="80ee1-114">PARAMETERS</span></span>

### <span data-ttu-id="80ee1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80ee1-115">-AsJob</span></span>
<span data-ttu-id="80ee1-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="80ee1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="80ee1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ee1-117">-DefaultProfile</span></span>
<span data-ttu-id="80ee1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ee1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80ee1-119">-InputObject</span></span>
<span data-ttu-id="80ee1-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80ee1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="80ee1-121">-Name</span></span>
<span data-ttu-id="80ee1-122">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ee1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80ee1-123">-NoWait</span></span>
<span data-ttu-id="80ee1-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="80ee1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80ee1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80ee1-125">-PassThru</span></span>
<span data-ttu-id="80ee1-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80ee1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ee1-127">-ResourceGroupName</span></span>
<span data-ttu-id="80ee1-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-128">The name of the resource group.</span></span>
<span data-ttu-id="80ee1-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ee1-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80ee1-130">-ServerName</span></span>
<span data-ttu-id="80ee1-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ee1-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80ee1-132">-SubscriptionId</span></span>
<span data-ttu-id="80ee1-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ee1-134">-확인</span><span class="sxs-lookup"><span data-stu-id="80ee1-134">-Confirm</span></span>
<span data-ttu-id="80ee1-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80ee1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80ee1-136">-WhatIf</span></span>
<span data-ttu-id="80ee1-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80ee1-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80ee1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ee1-139">CommonParameters</span></span>
<span data-ttu-id="80ee1-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ee1-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80ee1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ee1-142">입력</span><span class="sxs-lookup"><span data-stu-id="80ee1-142">INPUTS</span></span>

### <span data-ttu-id="80ee1-143">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="80ee1-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="80ee1-144">출력</span><span class="sxs-lookup"><span data-stu-id="80ee1-144">OUTPUTS</span></span>

### <span data-ttu-id="80ee1-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="80ee1-145">System.Boolean</span></span>

## <span data-ttu-id="80ee1-146">상속자</span><span class="sxs-lookup"><span data-stu-id="80ee1-146">NOTES</span></span>

<span data-ttu-id="80ee1-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="80ee1-147">ALIASES</span></span>

<span data-ttu-id="80ee1-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="80ee1-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80ee1-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80ee1-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="80ee1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80ee1-151">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="80ee1-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80ee1-152">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="80ee1-153">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="80ee1-154">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="80ee1-155">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="80ee1-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80ee1-156">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="80ee1-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="80ee1-158">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="80ee1-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="80ee1-160">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="80ee1-161">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="80ee1-162">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80ee1-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="80ee1-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80ee1-163">RELATED LINKS</span></span>
