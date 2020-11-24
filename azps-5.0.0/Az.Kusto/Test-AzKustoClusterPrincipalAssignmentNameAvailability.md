---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226896"
---
# <span data-ttu-id="e8d2f-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e8d2f-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="e8d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d2f-103">주 할당 이름이 유효 하며 아직 사용 중인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="e8d2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8d2f-104">SYNTAX</span></span>

### <span data-ttu-id="e8d2f-105">CheckExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e8d2f-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e8d2f-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e8d2f-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8d2f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e8d2f-107">DESCRIPTION</span></span>
<span data-ttu-id="e8d2f-108">주 할당 이름이 유효 하며 아직 사용 중인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="e8d2f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e8d2f-109">EXAMPLES</span></span>

### <span data-ttu-id="e8d2f-110">예제 1: 클러스터 위치 할당 이름 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="e8d2f-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="e8d2f-111">위의 명령은 "myprincipal" 이라는 PrincipalAssignment이 "testnewkustocluster" 클러스터에 있는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="e8d2f-112">예제 2: 클러스터 위치에서 사용 하지 않는 할당 이름 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="e8d2f-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="e8d2f-113">위의 명령은 "newprincipal" 이라는 PrincipalAssignment이 클러스터 "testnewkustocluster"에 있는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="e8d2f-114">변수</span><span class="sxs-lookup"><span data-stu-id="e8d2f-114">PARAMETERS</span></span>

### <span data-ttu-id="e8d2f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e8d2f-115">-ClusterName</span></span>
<span data-ttu-id="e8d2f-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d2f-117">-DefaultProfile</span></span>
<span data-ttu-id="e8d2f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8d2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8d2f-119">-InputObject</span></span>
<span data-ttu-id="e8d2f-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d2f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e8d2f-121">-Name</span></span>
<span data-ttu-id="e8d2f-122">Principal 배정 자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="e8d2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8d2f-124">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d2f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8d2f-125">-SubscriptionId</span></span>
<span data-ttu-id="e8d2f-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e8d2f-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d2f-128">-Type</span><span class="sxs-lookup"><span data-stu-id="e8d2f-128">-Type</span></span>
<span data-ttu-id="e8d2f-129">리소스 유형입니다 (Microsoft. Kusto/클러스터/-principalAssignments).</span><span class="sxs-lookup"><span data-stu-id="e8d2f-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d2f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e8d2f-130">-Confirm</span></span>
<span data-ttu-id="e8d2f-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8d2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8d2f-132">-WhatIf</span></span>
<span data-ttu-id="e8d2f-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8d2f-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8d2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d2f-135">CommonParameters</span></span>
<span data-ttu-id="e8d2f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d2f-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d2f-138">입력</span><span class="sxs-lookup"><span data-stu-id="e8d2f-138">INPUTS</span></span>

### <span data-ttu-id="e8d2f-139">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="e8d2f-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e8d2f-140">출력</span><span class="sxs-lookup"><span data-stu-id="e8d2f-140">OUTPUTS</span></span>

### <span data-ttu-id="e8d2f-141">Microsoft. Api20200614. ICheckNameResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="e8d2f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e8d2f-142">NOTES</span></span>

<span data-ttu-id="e8d2f-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="e8d2f-143">ALIASES</span></span>

<span data-ttu-id="e8d2f-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e8d2f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8d2f-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8d2f-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8d2f-147">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8d2f-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8d2f-148">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e8d2f-149">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e8d2f-150">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e8d2f-151">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e8d2f-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="e8d2f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8d2f-153">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e8d2f-154">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e8d2f-155">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e8d2f-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e8d2f-157">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d2f-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e8d2f-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8d2f-158">RELATED LINKS</span></span>
