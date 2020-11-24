---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311648"
---
# <span data-ttu-id="29b94-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="29b94-101">Get-AzAlert</span></span>

## <span data-ttu-id="29b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b94-102">SYNOPSIS</span></span>
<span data-ttu-id="29b94-103">알림 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="29b94-103">Get Alerts Information</span></span>

## <span data-ttu-id="29b94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29b94-104">SYNTAX</span></span>

### <span data-ttu-id="29b94-105">AlertsListByFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="29b94-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29b94-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="29b94-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29b94-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="29b94-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29b94-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29b94-108">DESCRIPTION</span></span>
<span data-ttu-id="29b94-109">**AzAlert** cmdlet이 발생 하는 경고 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="29b94-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29b94-110">EXAMPLES</span></span>

### <span data-ttu-id="29b94-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="29b94-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="29b94-112">Sev2 심각도 및 발생 한 모니터 조건의 모든 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="29b94-113">IncludeContext를 true로 설정 하려면 alert의 사용자 지정 페이로드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="29b94-114">Format-List를 사용 하 여 목록에서 각 알림에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="29b94-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="29b94-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="29b94-116">Id (GUID) 또는 리소스 Id를 기준으로 알림 세부 정보 가져오기 (전체 ARM Id)</span><span class="sxs-lookup"><span data-stu-id="29b94-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="29b94-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="29b94-117">Example 3</span></span>

<span data-ttu-id="29b94-118">알림 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-118">Get Alerts Information.</span></span> <span data-ttu-id="29b94-119">생성</span><span class="sxs-lookup"><span data-stu-id="29b94-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="29b94-120">변수</span><span class="sxs-lookup"><span data-stu-id="29b94-120">PARAMETERS</span></span>

### <span data-ttu-id="29b94-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="29b94-121">-AlertId</span></span>
<span data-ttu-id="29b94-122">알림의 알림/ResourceId에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="29b94-123">-AlertRuleId</span></span>
<span data-ttu-id="29b94-124">경고 규칙 Id에 대 한 필터</span><span class="sxs-lookup"><span data-stu-id="29b94-124">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="29b94-125">-CustomTimeRange</span></span>
<span data-ttu-id="29b94-126">지원 되는 형식- \<start-time\> / \<end-time\> 시간이 ISO에서 8601 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b94-127">-DefaultProfile</span></span>
<span data-ttu-id="29b94-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29b94-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="29b94-129">-IncludeContext</span></span>
<span data-ttu-id="29b94-130">알림의 컨텍스트 (사용자 지정 페이로드) 포함</span><span class="sxs-lookup"><span data-stu-id="29b94-130">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="29b94-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="29b94-132">기타 구성 포함</span><span class="sxs-lookup"><span data-stu-id="29b94-132">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="29b94-133">-MonitorCondition</span></span>
<span data-ttu-id="29b94-134">모니터 조건에 따라 필터링</span><span class="sxs-lookup"><span data-stu-id="29b94-134">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-135">-모니터 서비스</span><span class="sxs-lookup"><span data-stu-id="29b94-135">-MonitorService</span></span>
<span data-ttu-id="29b94-136">Moniter 서비스에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="29b94-136">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="29b94-137">-PageCount</span></span>
<span data-ttu-id="29b94-138">페이지에서 반입할 알림 수입니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-138">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-139">-선택</span><span class="sxs-lookup"><span data-stu-id="29b94-139">-Select</span></span>
<span data-ttu-id="29b94-140">필수 필드를 essentials 밖으로 프로젝트 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="29b94-141">필요한 입력은 쉼표로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-141">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-142">-심각도</span><span class="sxs-lookup"><span data-stu-id="29b94-142">-Severity</span></span>
<span data-ttu-id="29b94-143">알림의 심각도에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="29b94-143">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="29b94-144">-SmartGroupId</span></span>
<span data-ttu-id="29b94-145">스마트 그룹 Id를 갖는 모든 경고 필터링</span><span class="sxs-lookup"><span data-stu-id="29b94-145">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="29b94-146">-SortBy</span></span>
<span data-ttu-id="29b94-147">정렬 하는 동안 사용할 알림 속성</span><span class="sxs-lookup"><span data-stu-id="29b94-147">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="29b94-148">-SortOrder</span></span>
<span data-ttu-id="29b94-149">정렬 순서</span><span class="sxs-lookup"><span data-stu-id="29b94-149">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-150">-상태</span><span class="sxs-lookup"><span data-stu-id="29b94-150">-State</span></span>
<span data-ttu-id="29b94-151">알림의 상태에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="29b94-151">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29b94-152">-TargetResourceGroup</span></span>
<span data-ttu-id="29b94-153">경고 대상 리소스의 리소스 그룹 이름에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-153">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="29b94-154">-TargetResourceId</span></span>
<span data-ttu-id="29b94-155">경고 대상 리소스의 리소스 Id에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-155">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="29b94-156">-TargetResourceType</span></span>
<span data-ttu-id="29b94-157">경고 대상 리소스의 리소스 종류에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-157">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="29b94-158">-TimeRange</span></span>
<span data-ttu-id="29b94-159">지원 되는 시간 범위 값-1h, 1d, 7d, 30d (기본값은 1d)</span><span class="sxs-lookup"><span data-stu-id="29b94-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b94-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b94-160">CommonParameters</span></span>
<span data-ttu-id="29b94-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b94-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b94-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29b94-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b94-163">입력</span><span class="sxs-lookup"><span data-stu-id="29b94-163">INPUTS</span></span>

### <span data-ttu-id="29b94-164">않아야</span><span class="sxs-lookup"><span data-stu-id="29b94-164">None</span></span>

## <span data-ttu-id="29b94-165">출력</span><span class="sxs-lookup"><span data-stu-id="29b94-165">OUTPUTS</span></span>

### <span data-ttu-id="29b94-166">AlertsManagement 모델을 생성 합니다. PSAlert</span><span class="sxs-lookup"><span data-stu-id="29b94-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="29b94-167">상속자</span><span class="sxs-lookup"><span data-stu-id="29b94-167">NOTES</span></span>

## <span data-ttu-id="29b94-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29b94-168">RELATED LINKS</span></span>