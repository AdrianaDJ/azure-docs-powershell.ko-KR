---
title: Azure PowerShell 변경 로그 | Microsoft Docs
description: Azure PowerShell에 대한 최신 릴리스의 변경 내용입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826734"
---
# <a name="release-notes"></a><span data-ttu-id="f9d38-103">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="f9d38-103">Release notes</span></span>

<span data-ttu-id="f9d38-104">Azure PowerShell에 대한 릴리스의 변경 내용 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="f9d38-105">6.13.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="f9d38-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-106">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-107">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9d38-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9d38-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9d38-109">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f9d38-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f9d38-110">AzureRM.Automation</span></span>
* <span data-ttu-id="f9d38-111">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="f9d38-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f9d38-112">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f9d38-113">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f9d38-114">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f9d38-115">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-116">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-117">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f9d38-118">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="f9d38-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9d38-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="f9d38-120">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="f9d38-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9d38-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9d38-122">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-123">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-124">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f9d38-125">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f9d38-126">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f9d38-127">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9d38-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9d38-129">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f9d38-130">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f9d38-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f9d38-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f9d38-132">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="f9d38-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f9d38-133">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f9d38-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f9d38-134">AzureRM.Relay</span></span>
* <span data-ttu-id="f9d38-135">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-136">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-137">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="f9d38-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f9d38-138">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f9d38-139">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f9d38-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9d38-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9d38-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9d38-141">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-142">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-143">Azure Sql Database Managed Instance 및 Azure Sql 관리 데이터베이스에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f9d38-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9d38-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9d38-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9d38-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9d38-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9d38-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9d38-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9d38-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9d38-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9d38-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9d38-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9d38-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f9d38-152">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f9d38-153">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f9d38-154">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f9d38-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9d38-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f9d38-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9d38-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f9d38-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9d38-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f9d38-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9d38-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f9d38-159">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="f9d38-160">6.12.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="f9d38-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-161">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-162">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f9d38-163">Connect-AzureRmAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f9d38-164">Connect-AzureRmAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="f9d38-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="f9d38-165">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f9d38-166">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f9d38-167">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f9d38-168">연결되지 않은 경우 'Disconnect-AzureRmAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="f9d38-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f9d38-169">AzureRM.Automation</span></span>
* <span data-ttu-id="f9d38-170">cmdlet DLL 파일 이름이 Microsoft.Azure.Commands.Automation.dll로 변경됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f9d38-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f9d38-172">Get-AzureRmCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-173">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-174">Add-AzureRmVmssVMDataDisk 및 Remove-AzureRmVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f9d38-175">Get-AzureRmVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f9d38-176">수정된 SetAzureRmVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9d38-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9d38-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9d38-178">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f9d38-179">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f9d38-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f9d38-180">AzureRM.Insights</span></span>
* <span data-ttu-id="f9d38-181">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="f9d38-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f9d38-182">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="f9d38-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f9d38-183">해결된 문제 # 7513[자세한 정보] Set-AzureRMDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f9d38-184">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-185">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-186">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f9d38-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9d38-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f9d38-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f9d38-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f9d38-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9d38-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f9d38-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f9d38-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f9d38-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9d38-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f9d38-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9d38-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f9d38-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9d38-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f9d38-194">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9d38-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9d38-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9d38-196">복구 서비스에 Azure 파일 공유 지원 추가.</span><span class="sxs-lookup"><span data-stu-id="f9d38-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-197">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-198">https://github.com/Azure/azure-powershell/issues/7402에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f9d38-199">'Get-AzureRmResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="f9d38-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-201">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="f9d38-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9d38-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9d38-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9d38-203">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="f9d38-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f9d38-204">'Add-AzureRmServiceFabricClusterCertificate' 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f9d38-205">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="f9d38-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f9d38-206">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f9d38-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f9d38-207">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzureRmServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="f9d38-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="f9d38-208">6.11.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="f9d38-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-209">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-210">CloudShell에서 Get-AzureRmSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="f9d38-211">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="f9d38-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-212">AzureRM.Backup</span></span>
* <span data-ttu-id="f9d38-213">Azure Backup cmdlet이 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-214">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-215">'New-AzureRmVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="f9d38-216">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9d38-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9d38-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9d38-218">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f9d38-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f9d38-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f9d38-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에서 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f9d38-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-223">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-224">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f9d38-225">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-226">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-227">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzureRMRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f9d38-228">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="f9d38-229">2018년 10월 - 6.10.0</span><span class="sxs-lookup"><span data-stu-id="f9d38-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f9d38-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-230">Azure.Storage</span></span>
* <span data-ttu-id="f9d38-231">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f9d38-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9d38-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f9d38-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9d38-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f9d38-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f9d38-235">기존 계정이 없는 Get-AzureRmCognitiveServicesAccountSkus를 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-236">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-237">Get-AzureRmVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f9d38-238">'SimpleParameterSet' 예제가 New-AzureRmVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="f9d38-239">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9d38-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9d38-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9d38-241">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-242">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-243">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f9d38-244">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-244">new cmdlets added</span></span>
    - <span data-ttu-id="f9d38-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9d38-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f9d38-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9d38-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f9d38-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9d38-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f9d38-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9d38-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f9d38-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="f9d38-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f9d38-251">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f9d38-252">New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="f9d38-253">Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f9d38-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9d38-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f9d38-255">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="f9d38-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f9d38-256">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-257">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-258">-Mode 매개 변수를 Set-AzureRmPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="f9d38-259">사용자가 포함된 Origin 작업에서 Get-AzureRmProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-260">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-261">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f9d38-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-262">AzureRM.Storage</span></span>
* <span data-ttu-id="f9d38-263">특정 위치의 저장소 리소스 사용을 지원하고 글로벌 저장소 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f9d38-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f9d38-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-265">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-266">새 cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f9d38-267">새 cmdlet 
New-AzureRMWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="f9d38-268">6.9.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="f9d38-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9d38-269">일반</span><span class="sxs-lookup"><span data-stu-id="f9d38-269">General</span></span>
* <span data-ttu-id="f9d38-270">AzureRM.SignalR이 AzureRM 롤업 모듈에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-271">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-272">저장소 일반 코드에 대한 약간의 변경</span><span class="sxs-lookup"><span data-stu-id="f9d38-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="f9d38-273">전체 매개 변수 형식을 포함하도록 도움말 파일이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="f9d38-274">-ServicePrincipal을 필수가 아닌 것으로 ServicePrincipalCertificateWithSubscriptionId 매개변수 집합에서 변경</span><span class="sxs-lookup"><span data-stu-id="f9d38-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="f9d38-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-275">Azure.Storage</span></span>
* <span data-ttu-id="f9d38-276">OAuth를 사용하여 저장소 컨텍스트를 만드는 것을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="f9d38-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9d38-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f9d38-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9d38-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="f9d38-279">Cdn 가격 책정 sku에서 Standard_Microsoft를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-280">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-281">Keyvault 및 Storage에서 종속성을 일반 종속성으로 이동</span><span class="sxs-lookup"><span data-stu-id="f9d38-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="f9d38-282">AEM cmdlet에 더 많은 가상 머신 크기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="f9d38-283">PublicIPPrefix 매개 변수를 New-AzureRmVmssIpConfig에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f9d38-284">Invoke-AzureRmVMRunCommand cmdelt에 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="f9d38-285">Invoke-AzureRmVmssVMRunCommand cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f9d38-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f9d38-286">AzureRM.Dns</span></span>
* <span data-ttu-id="f9d38-287">Dns 레코드를 만드는 동안 별칭 레코드에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f9d38-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f9d38-288">AzureRM.Insights</span></span>
* <span data-ttu-id="f9d38-289">#6833 및 #7102 문제 수정(진단 설정 영역)</span><span class="sxs-lookup"><span data-stu-id="f9d38-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="f9d38-290">기본 이름, 즉 'service'에 진단 설정의 목록 생성 및 가져오는 동안에 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="f9d38-291">범주를 사용하는 진단 설정 만들기 문제</span><span class="sxs-lookup"><span data-stu-id="f9d38-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="f9d38-292">메트릭 시간 조직 매개 변수에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="f9d38-293">Timegrains 매개 변수는 여전히 받아들여지고 있습니다(이것은 호환성이 손상되는 변경이 아닙니다). 그러나 PT1M만 유효하므로 백엔드에서 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-294">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-295">LoadBalancer cmdlet에 대한 변경</span><span class="sxs-lookup"><span data-stu-id="f9d38-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="f9d38-296">LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp 및 EnableTcpReset 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="f9d38-297">LoadBalancerInboundNatRuleConfig: EnableTcpReset 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="f9d38-298">LoadBalancerRuleConfig: EnableTcpReset 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="f9d38-299">LoadBalancerProbeConfig: 매개 변수 프로토콜에 대해 "Https" 값에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="f9d38-300">새 LoadBalancer의 하위 리소스OutboundRule에 대한 새 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="f9d38-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f9d38-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f9d38-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f9d38-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f9d38-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="f9d38-306">PSNetworkInterface에 대한 새 HostedWorkloads 속성 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="f9d38-307">기능에 대한 새 cmdlet 추가: ARM을 통한 Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="f9d38-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="f9d38-308">Get-AzureRmFirewall 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="f9d38-309">Set-AzureRmFirewall 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="f9d38-310">New-AzureRmFirewall 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="f9d38-311">Remove-AzureRmFirewall 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="f9d38-312">New-AzureRmFirewallApplicationRuleCollection 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="f9d38-313">New-AzureRmFirewallApplicationRule 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="f9d38-314">New-AzureRmFirewallNatRuleCollection 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="f9d38-315">New-AzureRmFirewallNatRule 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="f9d38-316">New-AzureRmFirewallNetworkRuleCollection 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="f9d38-317">New-AzureRmFirewallNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="f9d38-318">Application Gateway에서 신뢰할 수 있는 루트 인증서 및 크기 자동 조정 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="f9d38-319">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="f9d38-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f9d38-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f9d38-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f9d38-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f9d38-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f9d38-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f9d38-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f9d38-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f9d38-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="f9d38-329">옵션 매개 변수를 사용하도록 업데이트된 Cmdlet-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="f9d38-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9d38-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f9d38-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9d38-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f9d38-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f9d38-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="f9d38-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f9d38-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="f9d38-334">옵션 매개 변수를 사용하도록 업데이트된 Cmdlet-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="f9d38-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9d38-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f9d38-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9d38-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="f9d38-337">인터페이스 엔드포인트 Get-AzureInterfaceEndpoint에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="f9d38-338">서브넷에서 여러 주소 접두사에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="f9d38-339">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="f9d38-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f9d38-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f9d38-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f9d38-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f9d38-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="f9d38-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f9d38-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f9d38-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f9d38-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f9d38-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f9d38-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f9d38-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="f9d38-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="f9d38-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="f9d38-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="f9d38-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f9d38-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f9d38-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f9d38-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f9d38-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="f9d38-359">서브넷 위임에 대한 cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="f9d38-360">New-AzureRmDelegation: 서브넷에 추가할 수 있는 새 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="f9d38-361">Remove-AzureRmDelegation: 서브넷에서 가져와서 해당 서브넷에서 제공된 위임 이름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="f9d38-362">Add-AzureRmDelegation: 서브넷에서 사용 및 제공된 서비스 이름을 해당 서브넷에 대한 위임으로 추가합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="f9d38-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="f9d38-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="f9d38-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="f9d38-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f9d38-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f9d38-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f9d38-366">관리되는 관리 디스크에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f9d38-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9d38-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f9d38-368">인사이트 종속성이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-369">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-370">New-AzureRmResourceGroupDeployment를 RollbackAction 새 매개 변수를 사용하여 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="f9d38-371">새 매개 변수를 사용하여 OnErrorDeployment에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="f9d38-372">정책 할당에서 관리되는 ID를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="f9d38-373">'New-AzureRmPolicyAssignment'를 사용하여 정책을 할당할 때 기본값이 있는 매개 변수는 더 이상 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="f9d38-374">정책 별칭을 검색하기 위한 새 cmdlet Get-AzureRmPolicyAlias 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-376">#7161 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="f9d38-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9d38-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="f9d38-378">SKU 이름을 Free_F1 및 Standard_S1로 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="f9d38-379">버전 필드를 PSSignalRResource 개체에 추가하고 연결 문자열을 PSSignalRKeys개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f9d38-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-380">AzureRM.Storage</span></span>
* <span data-ttu-id="f9d38-381">AzureRm.Storage에서 불변성 정책 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="f9d38-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9d38-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="f9d38-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9d38-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f9d38-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9d38-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f9d38-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9d38-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f9d38-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9d38-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f9d38-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f9d38-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="f9d38-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f9d38-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="f9d38-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9d38-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f9d38-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9d38-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f9d38-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9d38-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f9d38-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9d38-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-393">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-394">두 개의 새로운 cmdlet 추가: Get-AzureRmDeletedWebApp 및 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f9d38-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="f9d38-395">New-AzureRmAppServicePlan -HyperV 스위치가 창 컨테이너가 있는 앱 서비스 계획 작성용으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="f9d38-396">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows 컨테이너 앱을 만들고 관리하기 위한 새 매개 변수(-ContainerRegistryUser 문자열 -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="f9d38-397">6.8.1 - 2018년 8월</span><span class="sxs-lookup"><span data-stu-id="f9d38-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9d38-398">일반</span><span class="sxs-lookup"><span data-stu-id="f9d38-398">General</span></span>
* <span data-ttu-id="f9d38-399">기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f9d38-400">공용 런타임 어셈블리가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9d38-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9d38-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9d38-402">기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f9d38-403">문제 https://github.com/Azure/azure-powershell/issues/6603 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="f9d38-404">Import-AzureRmApiManagementApi 및 \*-AzureRmApiManagementCertificate cmdlet은 이제 상대 경로를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="f9d38-405">문제 https://github.com/Azure/azure-powershell/issues/6879 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="f9d38-406">CertificateInformation은 Set-AzureRmApiManagement cmdlet이 제대로 작동 하게 하는 설정 가능한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="f9d38-407">4.0.4-preview nuget으로 업그레이드하여 해결됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="f9d38-408">문제 https://github.com/Azure/azure-powershell/issues/6853 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="f9d38-409">제품에서 이름별 검색에 대해 Odata 필터가 수정됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="f9d38-410">문제 https://github.com/Azure/azure-powershell/issues/6814 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="f9d38-411">API에서 이름별 검색에 대해 Odata 필터가 수정됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="f9d38-412">AzureMonitor 로거에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-413">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-414">오류 출력에 대상이 없는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="f9d38-415">관리 디스크를 사용하는 VM에 대한 저장소 계정 유형 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="f9d38-416">기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f9d38-417">예를 들어 Azure 중국과 같이, 다른 환경에 대한 AEM 확장 cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-418">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-419">기본 cmdlet 출력 표시를 테이블 뷰로 변경</span><span class="sxs-lookup"><span data-stu-id="f9d38-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f9d38-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9d38-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9d38-421">일시 중지된 용량을 확장하려고 할 때 Update-AzureRmPowerBIEmbeddedCapacity 실패 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="f9d38-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-422">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-423">MarketPlace에서 관리되는 응용 프로그램 생성 시의 문제 해결.</span><span class="sxs-lookup"><span data-stu-id="f9d38-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-425">해결된 문제</span><span class="sxs-lookup"><span data-stu-id="f9d38-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9d38-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9d38-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9d38-427">다중값 라우팅 메서드에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="f9d38-428">다중값 라우팅에 대한 새 매개 변수 'MaxReturn'</span><span class="sxs-lookup"><span data-stu-id="f9d38-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="f9d38-429">서브넷 라우팅 메서드에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="f9d38-430">엔드포인트의 IP 주소 범위(서브넷)에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="f9d38-431">프로필 내 사용자 지정 헤더에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="f9d38-432">프로필 내 예상 상태 코드 범위에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="f9d38-433">엔드포인트 내 사용자 지정 헤더에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="f9d38-434">6.8.0 - 2018년 8월</span><span class="sxs-lookup"><span data-stu-id="f9d38-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9d38-435">일반</span><span class="sxs-lookup"><span data-stu-id="f9d38-435">General</span></span>
* <span data-ttu-id="f9d38-436">기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-437">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-438">Connect-AzureRmAccount 중에 반환된 토큰에 만료 속성 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-439">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-440">오류 출력에 대상이 없는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="f9d38-441">관리 디스크를 사용하는 VM에 대한 저장소 계정 유형 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="f9d38-442">예를 들어 Azure 중국과 같이, 다른 환경에 대한 AEM 확장 cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f9d38-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9d38-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="f9d38-444">New-AzureRmIotHubExportDevices 및 New-AzureRmIotHubImportDevices에 대한 예제를 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-445">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-446">기본 모델 표시를 테이블 뷰로 변경</span><span class="sxs-lookup"><span data-stu-id="f9d38-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f9d38-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9d38-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9d38-448">일시 중지된 용량을 확장하려고 할 때 Update-AzureRmPowerBIEmbeddedCapacity 실패 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-449">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-450">MarketPlace에서 관리되는 응용 프로그램 생성 시의 문제 해결.</span><span class="sxs-lookup"><span data-stu-id="f9d38-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-452">문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9d38-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9d38-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9d38-454">다중값 라우팅 메서드에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="f9d38-455">다중값 라우팅에 대한 새 매개 변수 'MaxReturn'</span><span class="sxs-lookup"><span data-stu-id="f9d38-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="f9d38-456">서브넷 라우팅 메서드에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="f9d38-457">엔드포인트의 IP 주소 범위(서브넷)에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="f9d38-458">프로필 내 사용자 지정 헤더에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="f9d38-459">프로필 내 예상 상태 코드 범위에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="f9d38-460">엔드포인트 내 사용자 지정 헤더에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-461">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-462">기본 리소스 그룹이 잘못 설정되는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="f9d38-463">6.7.0 - 2018년 8월</span><span class="sxs-lookup"><span data-stu-id="f9d38-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-464">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-465">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9d38-466">충돌을 방지하려면 기본 컨텍스트 이름으로 사용자 ID를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="f9d38-467">#6398 컨텍스트를 선택할 때 문제를 발생시킨 Clear-AzureRmContext 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="f9d38-468">'Connect-AzureRmAccount'에 대한 '-TenantId' 매개 변수에 전달할 테넌트 도메인을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="f9d38-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="f9d38-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-469">Azure.Storage</span></span>
* <span data-ttu-id="f9d38-470">Azure 파일 공유 할당량에 대한 5TB 제한 제거</span><span class="sxs-lookup"><span data-stu-id="f9d38-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="f9d38-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f9d38-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9d38-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9d38-473">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="f9d38-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="f9d38-475">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9d38-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9d38-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9d38-477">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="f9d38-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f9d38-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="f9d38-479">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f9d38-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f9d38-480">AzureRM.Automation</span></span>
* <span data-ttu-id="f9d38-481">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="f9d38-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-482">AzureRM.Backup</span></span>
* <span data-ttu-id="f9d38-483">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f9d38-484">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-484">AzureRM.Batch</span></span>
* <span data-ttu-id="f9d38-485">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="f9d38-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="f9d38-486">AzureRM.Billing</span></span>
* <span data-ttu-id="f9d38-487">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f9d38-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9d38-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="f9d38-489">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f9d38-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f9d38-491">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-492">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-493">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9d38-494">New-AzureRmVmssConfig에 EvictionPolicy 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="f9d38-495">지정된 위치가 없는 경우에 New-AzureRmVm의 DiskFileParameterSet 내의 기본 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="f9d38-496">Save-AzureRmVMImage에서 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f9d38-497">특정 singlepass 관련 시나리오에 대해 Get-AzureRmVMDiskEncryptionStatus cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f9d38-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f9d38-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="f9d38-499">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="f9d38-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9d38-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="f9d38-501">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="f9d38-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9d38-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="f9d38-503">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="f9d38-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f9d38-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="f9d38-505">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9d38-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9d38-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9d38-507">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f9d38-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9d38-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f9d38-509">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9d38-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9d38-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9d38-511">DebugPreference가 powershell 명령줄에서 설정된 경우 디버깅 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="f9d38-512">Set-AzureRmDataLakeStoreItemAcl에 대한 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f9d38-513">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9d38-514">Set-AzureRmDataLakeStoreItemAclEntry에 대한 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="f9d38-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f9d38-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="f9d38-516">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f9d38-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f9d38-517">AzureRM.Dns</span></span>
* <span data-ttu-id="f9d38-518">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f9d38-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9d38-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f9d38-520">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9d38-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9d38-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9d38-522">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="f9d38-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9d38-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="f9d38-524">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f9d38-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f9d38-525">AzureRM.Insights</span></span>
* <span data-ttu-id="f9d38-526">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f9d38-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9d38-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="f9d38-528">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9d38-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9d38-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9d38-530">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f9d38-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9d38-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f9d38-532">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="f9d38-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9d38-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="f9d38-534">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="f9d38-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f9d38-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="f9d38-536">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="f9d38-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9d38-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9d38-538">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="f9d38-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="f9d38-539">AzureRM.Media</span></span>
* <span data-ttu-id="f9d38-540">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-541">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-542">Set-AzureRmLocalNetworkGateway에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="f9d38-543">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey, New-AzureRmVirtualNetworkGatewayConnection에 대한 예제 및 설명 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9d38-544">Remove-AzureRmVirtualNetworkGatewayIpConfig 및 Reset-AzureRmVirtualNetworkGateway에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="f9d38-545">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f9d38-546">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f9d38-547">Set-AzureRmVirtualNetworkGatewayConnection에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9d38-548">최신 코드 생성기를 사용하여 ApplicationSecurityGroup, RouteTable 및 Usage에 대한 cmdlet을 다시 생성함</span><span class="sxs-lookup"><span data-stu-id="f9d38-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="f9d38-549">Exitc 하지 않는 서브넷을 얻으려고 할 때의 Get-AzureRmVirtualNetworkSubnetConfig에 대한 오류 메시지를 설명</span><span class="sxs-lookup"><span data-stu-id="f9d38-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="f9d38-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f9d38-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="f9d38-551">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="f9d38-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9d38-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f9d38-553">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f9d38-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9d38-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f9d38-555">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f9d38-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9d38-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9d38-557">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="f9d38-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="f9d38-559">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9d38-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9d38-561">Get-AzureRmRecoveryServicesBackItem cmdlet에 정책 필터 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="f9d38-562">해당 명령은 지정된 정책 ID에 의해 보호되는 백업 항목의 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="f9d38-563">Microsoft.Azure.Management.RecoveryServices.Backup을 버전 3.0.0-preview로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="f9d38-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="f9d38-564">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f9d38-565">Restore-AzureRmRecoveryServicesBackupItem에 TargetResourceGroupName 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="f9d38-566">관리 디스크가 복원될 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="f9d38-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="f9d38-567">관리 디스크가 있는 VM의 백업에 적용 가능</span><span class="sxs-lookup"><span data-stu-id="f9d38-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f9d38-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f9d38-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f9d38-569">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f9d38-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9d38-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f9d38-571">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f9d38-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f9d38-572">AzureRM.Relay</span></span>
* <span data-ttu-id="f9d38-573">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-574">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-575">구독 범위에서 템플릿 배포를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="f9d38-576">새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="f9d38-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="f9d38-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9d38-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9d38-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9d38-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9d38-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9d38-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9d38-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9d38-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9d38-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f9d38-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="f9d38-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f9d38-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="f9d38-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f9d38-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="f9d38-584">Set-AzureRmResource에 컨텍스트를 전달할 때 오류가 발생하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="f9d38-585">New-AzureRmResourceGroupDeployment의 예제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="f9d38-586">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f9d38-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f9d38-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f9d38-588">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-590">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9d38-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9d38-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9d38-592">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-593">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-594">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f9d38-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-595">AzureRM.Storage</span></span>
* <span data-ttu-id="f9d38-596">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="f9d38-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9d38-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="f9d38-598">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f9d38-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f9d38-599">AzureRM.Tags</span></span>
* <span data-ttu-id="f9d38-600">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9d38-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9d38-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9d38-602">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="f9d38-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f9d38-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="f9d38-604">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-605">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-606">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="f9d38-607">6.6.0 - 2018년 7월</span><span class="sxs-lookup"><span data-stu-id="f9d38-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9d38-608">일반</span><span class="sxs-lookup"><span data-stu-id="f9d38-608">General</span></span>
* <span data-ttu-id="f9d38-609">전체 매개 변수 형식 및 올바른 입/출력 형식을 포함하도록 모든 도움말 파일을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-610">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-611">Common.Strategy 라이브러리가 리소스에 대한 현재 구성이 대상 리소스와 호환되는지 유효성을 검사할 수 있도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="f9d38-612">Common.Storage에 ps1xml 형식 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f9d38-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-613">Azure.Storage</span></span>
* <span data-ttu-id="f9d38-614">DefaultProfile에서 저장소 컨텍스트를 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="f9d38-615">Ps1XmlAttribute를 cmdlet 출력 형식 속성에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9d38-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9d38-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9d38-617">문제 https://github.com/Azure/azure-powershell/issues/6370 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="f9d38-618">PsApiManagementApi를 ApiContract로 좌표 이동하도록 Automapper 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="f9d38-619">문제 https://github.com/Azure/azure-powershell/issues/6515 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="f9d38-620">인코딩 형식을 사용하여 오버로드하지 않도록 File.Save 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="f9d38-621">문제 https://github.com/Azure/azure-powershell/issues/6560 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="f9d38-622">apiId에서 패턴 예외를 수정하는 4.0.3 Nuget 버전으로 업그레이드됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-623">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-624">PremiumLRS 저장소 계정 형식 이름 바꾸기로 인해 New-AzureRmVm에서 DiskFileParameterSet를 사용하여 vm 생성 시 실패하는 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="f9d38-625">Invoke-AzureRmVMRunCommand cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="f9d38-626">Get-AzureRmAvailabilitySet를 업데이트하여 구독에서 모든 가용성 집합 리스트를 사용하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="f9d38-627">(ResouceGroupName 매개 변수는 이제 선택적 요소입니다.)</span><span class="sxs-lookup"><span data-stu-id="f9d38-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="f9d38-628">vm 선별에 가속화된 네트워크를 사용하도록 'New-AzureRmVm'의 SimpleParameterSet를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="f9d38-629">New-AzureRmVmss 간단 매개 변수가 사용자 지정 LB가 이미 존재할 때 vms 생성에 실패하도록 설정하여 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="f9d38-630">New-AzureRmDisk에 대한 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="f9d38-631">'New-AzureRmVM'에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="f9d38-632">Set-AzureRmVMOSDisk에 대한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="f9d38-633">Set-AzureRmVMBginfoExtension 맞춤법 및 접두사를 수정하도록 예제 1을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9d38-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9d38-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9d38-635">ADF.Net SDK 버전을 1.1.0으로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="f9d38-636">데이터 팩터리를 공유하는 자체 호스팅된 통합 런타임을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="f9d38-637">새 매개 변수 -SharedIntegrationRuntimeResourceId를 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet에 추가.</span><span class="sxs-lookup"><span data-stu-id="f9d38-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="f9d38-638">새로운 선택적 매개 변수 -LinkedDataFactoryName을 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet에 추가.</span><span class="sxs-lookup"><span data-stu-id="f9d38-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9d38-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9d38-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9d38-640">DataPlane SDK(Microsoft.Azure.DataLake.Store) 버전을 1.1.9로 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9d38-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9d38-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9d38-642">cmdlet 제거에서 InputObject 및 ResourceId에 대한 파이핑이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f9d38-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f9d38-643">AzureRM.Insights</span></span>
* <span data-ttu-id="f9d38-644">도움말 파일에서 OutputType 서식 지정 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="f9d38-645">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview를 사용</span><span class="sxs-lookup"><span data-stu-id="f9d38-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9d38-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9d38-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9d38-647">Set-AzureRmKeyVaultAccessPolicy 내 파이핑 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-648">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-649">LoadBalancerInboundNatPoolConfig cmdlet에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-650">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-651">'Get-AzureRmResource'에 대한 태그 이름 및 값을 제공할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="f9d38-652">'Set-AzureRmResource'를 사용하여 파이핑 시나리오 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-654">cmdlet 제거에서 InputObject 및 ResourceId에 대한 파이핑이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="f9d38-655">몇 가지 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-656">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-657">다음 cmdlet 사용하여 서버 Advanced Threat Protection 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="f9d38-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9d38-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f9d38-659">다음 cmdlet을 사용하여 취약성 평가 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="f9d38-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="f9d38-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="f9d38-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="f9d38-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="f9d38-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="f9d38-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="f9d38-663">Remove-AzureRmSqlServerFirewallRule의 예제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="f9d38-664">Get-AzureSqlSyncGroupLog에서 미국이 아닌 문화권에서 날짜/시간을 올바르지 않게 다루는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f9d38-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-665">AzureRM.Storage</span></span>
* <span data-ttu-id="f9d38-666">Ps1XmlAttribute를 cmdlet 출력 형식 속성에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="f9d38-667">StorageAccount cmdlet 출력을 테이블 뷰로 표시</span><span class="sxs-lookup"><span data-stu-id="f9d38-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="f9d38-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9d38-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f9d38-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9d38-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f9d38-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9d38-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f9d38-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f9d38-671">AzureRM.Tags</span></span>
* <span data-ttu-id="f9d38-672">태그 cmdlet 도움말에서 잘못된 문을 제거합니다</span><span class="sxs-lookup"><span data-stu-id="f9d38-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="f9d38-673">6.5.0 - 2018년 7월</span><span class="sxs-lookup"><span data-stu-id="f9d38-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-674">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-675">'Get-AzureRmContextAutosaveSetting'에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f9d38-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-676">Azure.Storage</span></span>
* <span data-ttu-id="f9d38-677">쓰기 전용 SaS 토큰을 사용하는 Blob 또는 파일 업로드 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="f9d38-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9d38-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="f9d38-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9d38-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9d38-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9d38-681">필수 속성 ResourceGroupName을 AS에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f9d38-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f9d38-682">AzureRM.Automation</span></span>
* <span data-ttu-id="f9d38-683">도움말을 업데이트하고 'New-AzureRMAutomationSchedule'에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-684">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-685">-Tag 매개 변수를 Update/New-AzureRmAvailabilitySet에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="f9d38-686">‘Add-AzureRmVmssExtension’에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f9d38-687">‘Remove-AzureRmVmssExtension’에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f9d38-688">‘Set-AzureRmVMAccessExtension’에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="f9d38-689">기본으로 SinglePlacementGroup을 false로 설정하고 단일 배치 그룹에 VMSS를 만들 수 있는 스위치 매개 변수 'SinglePlacementGroup'을 추가하도록 New-AzureRmVmss에 대한 SimpleParameterSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9d38-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9d38-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9d38-691">PSEventHubDRConfigurationAttributes 클래스에 읽기 전용 속성 'PendingReplicationOperationsCount'를 추가하여 복제가 진행되는 동안 보류 중인 복제 작업 수를 제공</span><span class="sxs-lookup"><span data-stu-id="f9d38-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9d38-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9d38-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9d38-693">Set-AzureRmKeyVaultAccessPolicy에 대한 오류 메시지 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f9d38-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9d38-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f9d38-695">New-AzureRmLogicApp에서 "매개 변수 집합을 확인할 수 없습니다" 오류 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-696">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-697">Set/Add-AzureRmVirtualNetworkPeering에 대한 여러 테넌트의 가상 네트워크에서 피어링을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="f9d38-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="f9d38-698">Application Gateway에 대한 아래 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="f9d38-699">New-AzureRmApplicationGateway: EnableFIPS 플래그 및 영역 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="f9d38-700">New-AzureRmApplicationGatewaySku: 새 sku Standard_v2 및 WAF_v2 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="f9d38-701">Set-AzureRmApplicationGatewaySku: 새 sku Standard_v2 및 WAF_v2 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="f9d38-702">최신 생성기를 사용하여 RouteTable cmdlet을 재생성</span><span class="sxs-lookup"><span data-stu-id="f9d38-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f9d38-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f9d38-703">AzureRM.Relay</span></span>
* <span data-ttu-id="f9d38-704">markdown 파일을 업데이트하여 예제에서 매개 변수 이름 문제에 대해 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-705">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-706">Roledefinition 및 Roleassignment cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="f9d38-707">페이징의 일부분으로 수행하는 추가 roledefinition 호출을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="f9d38-708">Get-AzureRmRoleAssignment cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="f9d38-709">-ExpandPrincipalGroups 명령 매개 변수 기능 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="f9d38-710">'Get-AzureRmResource'에서 '-ResourceType' 매개 변수가 대/소문자를 구분하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-712">top 및 skip 매개 변수가 cmdlet 목록을 나열하도록 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="f9d38-713">표준을 프리미엄 네임스페이스 마이그레이션 cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="f9d38-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9d38-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9d38-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9d38-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9d38-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9d38-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9d38-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9d38-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f9d38-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f9d38-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="f9d38-719">PSServiceBusDRConfigurationAttributes 클래스에 읽기 전용 속성 'PendingReplicationOperationsCount'를 추가하여 복제가 진행되는 동안 보류 중인 복제 작업 수를 제공</span><span class="sxs-lookup"><span data-stu-id="f9d38-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9d38-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9d38-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9d38-721">‘New-AzureRmServiceFabricCluster’에 대한 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-722">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-723">Management.Sql에 대한 새 cmdlet을 추가하여 고객이 TDE 인증서를 SQL Server 인스턴스 또는 Managed Instance에 추가할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="f9d38-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="f9d38-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="f9d38-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-726">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-727">`Set-AzureRmWebApp -AssignIdentity` 및 `Set-AzureRmWebAppSlot -AssignIdentity`가 false로 설정되면 사이트 개체에서 Identity 속성이 제거됩니다. 미리보기 태그도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="f9d38-728">`Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics` 예제가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="f9d38-729">`Set-AzureRmWebApp -PhpVersion`이 유효한 php 버전으로 해제 지원</span><span class="sxs-lookup"><span data-stu-id="f9d38-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="f9d38-730">6.4.0 - 2018년 7월</span><span class="sxs-lookup"><span data-stu-id="f9d38-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9d38-731">일반</span><span class="sxs-lookup"><span data-stu-id="f9d38-731">General</span></span>
* <span data-ttu-id="f9d38-732">대부분의 모듈에 대한 도움말 파일에서 OutputType 서식 지정 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-733">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-734">기본 출력 형식에 추가된 Ps1Xml 특성</span><span class="sxs-lookup"><span data-stu-id="f9d38-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-735">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-736">VMSS에 대한 IP 태그 기능</span><span class="sxs-lookup"><span data-stu-id="f9d38-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="f9d38-737">'New-AzureRmVmssIpTagConfig' cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="f9d38-738">New-AzureRmVmssIpConfig에 IpTag 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f9d38-739">VMSS에 대한 자동 OS 롤백 기능</span><span class="sxs-lookup"><span data-stu-id="f9d38-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="f9d38-740">New-AzureRmVmssConfig 및 Update-AzureRmVmss에 DisableAutoRollback 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="f9d38-741">Vmss에 대한 OS 업그레이드 기록 기능</span><span class="sxs-lookup"><span data-stu-id="f9d38-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="f9d38-742">Get-AzureRmVmss에 OSUpgradeHistory 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f9d38-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9d38-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f9d38-744">다음 명령을 통해 카탈로그 액세스 제어 목록에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="f9d38-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9d38-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f9d38-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9d38-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f9d38-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f9d38-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9d38-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9d38-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9d38-749">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl에 대한 취소 지원 및 진행률 추적 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f9d38-750">Export-AzureRmDataLakeStoreChildItemProperties에 대한 취소 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f9d38-751">재귀 작업을 수행하는 cmdlet에 대한 디버그 메시지 플러시 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="f9d38-752">DataLake cmdlet의 테스트 위치 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f9d38-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9d38-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="f9d38-754">목록 작업 cmdlet Get-AzureRmEventHub 및 Get-AzureRmEventHubConsumerGroup에 선택적 MaxCount 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="f9d38-755">새 EventHub 만드는 동안 하나 이상의 매개 변수가 필요한 New-AzureRmEventHub cmdlet 문제를 해결.</span><span class="sxs-lookup"><span data-stu-id="f9d38-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="f9d38-756">기본 매개 변수 집합을 제공.</span><span class="sxs-lookup"><span data-stu-id="f9d38-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="f9d38-757">선택적 매개 변수 -KeyValue를 New-AzureRmEventHubKey cmdlet에 추가 하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9d38-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9d38-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9d38-759">Get-AzureRmKeyVault -Tag 실행 시 모든 리소스가 리턴되는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-760">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-761">영역 중복 VirtualNetworkGateways에 대한 새 Sku를 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="f9d38-762">기능에 대한 새 명령이 추가됨: ARM을 통한 ExpressRoute Partner APIs</span><span class="sxs-lookup"><span data-stu-id="f9d38-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="f9d38-763">Get- AzureRmExpressRouteCrossConnection 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f9d38-764">Set-AzureRmExpressRouteCrossConnection 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f9d38-765">Add-AzureRmExpressRouteCrossConnectionPeering 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f9d38-766">Get-AzureRmExpressRouteCrossConnectionPeering 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f9d38-767">Remove-AzureRmExpressRouteCrossConnectionPeering 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f9d38-768">Get-AzureRMExpressRouteCrossConnectionArpTable 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f9d38-769">Get-AzureRMExpressRouteCrossConnectionRouteTable 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f9d38-770">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9d38-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9d38-772">Get-AzureRmRecoveryServicesBackupStatus cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="f9d38-773">이 cmdlet은 VM ID를 가져와서 VM이 구독에서 일부 자격 증명 모음으로 보호되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="f9d38-774">이러한 자격 증명 모음이 존재하는 경우 cmdlet은 자격 증명 모음 세부 정보를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-775">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-776">Get-AzureRmPolicyAssignment cmdlet을 다음과 같이 업데이트함.</span><span class="sxs-lookup"><span data-stu-id="f9d38-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="f9d38-777">관리 그룹 수준에서 -Scope 값 리스팅에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="f9d38-778">관리 그룹 수준에서 -Scope 값을 사용하여 개별 할당값을 검색하는 것에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="f9d38-779">제어 매개 변수에 -Effective 및 -All 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="f9d38-780">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="f9d38-781">지정된 관리 그룹에 작업을 적용할 -ManagementGroupName 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f9d38-782">지정된 구독에 작업을 적용할 -SubscriptionId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f9d38-783">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="f9d38-784">지정된 관리 그룹에 작업을 적용할 -ManagementGroupName 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f9d38-785">지정된 구독에 작업을 적용할 -SubscriptionId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f9d38-786">'New-AzureRmResourceGroupDeployment'에서 'TemplateParameterObject'를 사용하는 경우 매개 변수에 KeyVault 비밀 참조 지원 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="f9d38-787">'New-AzureRmADAppCredential'에 대해 '-EndDate' 매개 변수가 무시되는 문제를 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="f9d38-788">'Add-AzureRmADGroupMember'가 요청에 잘못된 URL을 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="f9d38-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9d38-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f9d38-790">선택적 매개 변수 -KeyValue를 New-AzureRmServiceBusKey cmdlet에 추가 하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-791">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-792">New-AzureRmSqlDatabaseRestorePoint 도움말에서 SQLDW에 대한 사용자 정의 복원 지점 명시</span><span class="sxs-lookup"><span data-stu-id="f9d38-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="f9d38-793">몇 가지 cmdlet에서-ComputeGeneration 매개 변수의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="f9d38-794">6.3.0 - 2018년 6월</span><span class="sxs-lookup"><span data-stu-id="f9d38-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-795">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-796">Enable-AzureRmContextAutoSave에 대한 오류 메시지 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="f9d38-797">이전 컨텍스트 없이 'Connect-AzureRmAccount' 실행 시 각 구독에 대한 컨텍스트 생성</span><span class="sxs-lookup"><span data-stu-id="f9d38-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f9d38-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f9d38-798">Azure.Storage</span></span>
* <span data-ttu-id="f9d38-799">도움말 파일 내 -Permissions 매개 변수에 대한 추가 정보가 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-800">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-801">'Get-AzureRmVmDiskEncryptionStatus'가 데이터 디스크가 없는 VM에 대해 관찰된 문제를 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="f9d38-802">Compute 클라이언트 라이브러리 버전을 업데이트하여 다음 cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="f9d38-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f9d38-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f9d38-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f9d38-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f9d38-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f9d38-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f9d38-806">다음 cmdlet이 '작업 ID' 및 '작업 상태'를 올바르게 표시하도록 수정:</span><span class="sxs-lookup"><span data-stu-id="f9d38-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="f9d38-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9d38-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="f9d38-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9d38-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="f9d38-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9d38-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="f9d38-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f9d38-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="f9d38-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="f9d38-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="f9d38-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9d38-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="f9d38-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f9d38-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="f9d38-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f9d38-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="f9d38-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9d38-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="f9d38-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9d38-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="f9d38-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9d38-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="f9d38-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f9d38-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="f9d38-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f9d38-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="f9d38-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f9d38-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f9d38-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f9d38-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="f9d38-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f9d38-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f9d38-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f9d38-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="f9d38-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f9d38-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="f9d38-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f9d38-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f9d38-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9d38-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f9d38-827">Update-AzureRmEventGridSubscription cmdlet의 SubjectBeginsWith/SubjectEndsWith에 대한 ValidateNotNullOrEmpty 유효성 검사 조건을 제거하여 필요에 따라 이러한 매개 변수를 빈 문자열로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f9d38-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9d38-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9d38-829">Get-AzureRmKeyVault -Tag 실행 시 태그가 리턴되지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f9d38-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9d38-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f9d38-831">Policy Insights cmdlet의 공개 릴리스</span><span class="sxs-lookup"><span data-stu-id="f9d38-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="f9d38-832">API 버전 2018-04-04 사용</span><span class="sxs-lookup"><span data-stu-id="f9d38-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="f9d38-833">PolicyDefinitionReferenceId를 Get-AzureRmPolicyStateSummary의 결과 집합에 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f9d38-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9d38-835">-Vault 매개 변수를 RecoveryServices.Backup cmdlet에 추가.</span><span class="sxs-lookup"><span data-stu-id="f9d38-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="f9d38-836">전달되는 경우 이는 Set-AzureRmRecoveryServicesContext cmdlet을 재정의함.</span><span class="sxs-lookup"><span data-stu-id="f9d38-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-837">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-838">Get-AzureRmSqlDatabaseExpanded에 대한 도움말 파일의 예가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9d38-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9d38-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9d38-840">Add-AzureRmTrafficManagerEndpointConfig에대한 도움말 파일이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-841">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-842">-AssignIdentity를 사용할 때 AppSetting을 덮어쓰지 않도록 'Set-AzureRmWebApp'이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="f9d38-843">'New-AzureRmWebAppSlot'이 AppServicePlan을 옵션 매개변수로 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="f9d38-844">6.2.1 - 2018년 6월</span><span class="sxs-lookup"><span data-stu-id="f9d38-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="f9d38-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9d38-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f9d38-846">PSWorkspace 모델이 Network 형식을 매개 변수로 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="f9d38-847">6.2.0 - 2018년 6월</span><span class="sxs-lookup"><span data-stu-id="f9d38-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-848">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-849">Newtonsoft.Json의 버전 10.0.3이 모듈 가져오기에 로드되지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f9d38-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f9d38-850">AzureRM.Compute</span></span>
* <span data-ttu-id="f9d38-851">VMSS VM 업데이트 기능</span><span class="sxs-lookup"><span data-stu-id="f9d38-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="f9d38-852">'Update-AzureRmVmssVM' 및 'New-AzureRmVMDataDisk' cmdlets 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="f9d38-853">데이터 디스크를 Vmss VM에 추가할 수 있도록 지원하기 위해 VirtualMachineScaleSetVM 매개변수를 'Add-AzureRmVMDataDisk' cmdlet에 추가하였습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f9d38-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9d38-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f9d38-855">ADF .Net SDK 버전이 다음 변경 내용이 포함된 0.8.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f9d38-856">팩터리 리포지토리 작업 구성 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="f9d38-857">QuickBooks LinkedService가 ConsumerKey 및 consumerSecret 속성을 노출하도록 업데이트됨 </span><span class="sxs-lookup"><span data-stu-id="f9d38-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="f9d38-858">여러 모델 유형을 SecretBase에서 개체로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="f9d38-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="f9d38-859">Blob 이벤트 트리거 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f9d38-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9d38-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f9d38-861">예제 출력으로 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-862">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-863">Network Watcher cmdlet에서 트래픽 분석 매개 변수를 사용가능하도록 설정</span><span class="sxs-lookup"><span data-stu-id="f9d38-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f9d38-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f9d38-864">AzureRM.Resources</span></span>
* <span data-ttu-id="f9d38-865">'Get AzureRmResource'에서 반환된 'PSResource' 개체의 'Properties' 속성의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f9d38-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f9d38-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f9d38-867">ServiceBusQueueJob 업데이트가 새 인증 값을 설정하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="f9d38-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="f9d38-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-868">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-869">옵션 LicenseType 매개 변수를 사용하여 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9d38-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="f9d38-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f9d38-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9d38-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f9d38-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f9d38-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f9d38-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f9d38-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f9d38-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f9d38-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f9d38-875">AzureRM.Websites</span></span>
* <span data-ttu-id="f9d38-876">'New-AzureRMWebApp'이 전략 라이브러리의 공통 알고리즘을 사용하도록 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="f9d38-877">6.1.0 - 2018년 5월</span><span class="sxs-lookup"><span data-stu-id="f9d38-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9d38-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9d38-878">AzureRM.Profile</span></span>
* <span data-ttu-id="f9d38-879">'Clear-AzureRmContext'를 실행하면 이전 기본 컨텍스트의 이름으로 빈 컨텍스트가 유지되어 사용자가 이전 이름으로 새 컨텍스트를 만들지 못하게 되는 문제를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9d38-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9d38-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9d38-881">AS에서 게이트웨이가 작업을 연결하거나 연결 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9d38-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9d38-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9d38-883">ApiVersions, ApiReleases 및 ApiRevisions에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f9d38-884">ServiceFabric 백 엔드에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f9d38-885">Application Insights 로거에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f9d38-886">'기본' SKU를 API Management 서비스의 유효한 SKU로 인식하는 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f9d38-887">개인 CA가 발급한 인증서를 루트 또는 CA로 설치하는 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f9d38-888">KeyVault 및 다중 프록시 호스트 이름을 통한 사용자 정의 SSL 인증서를 수락하는 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f9d38-889">MSI ID에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="f9d38-889">Added support for MSI identity</span></span>
* <span data-ttu-id="f9d38-890">URL을 통한 정책을 수락하는 지원 추가됨 참고: 다음 cmdlet은 이후 릴리스에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f9d38-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d38-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f9d38-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f9d38-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f9d38-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f9d38-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f9d38-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f9d38-895">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f9d38-895">AzureRM.Batch</span></span>
* <span data-ttu-id="f9d38-896">새 cmdlet Get AzureBatchPoolNodeCounts 릴리스</span><span class="sxs-lookup"><span data-stu-id="f9d38-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f9d38-897">새 cmdlet Start-AzureBatchComputeNodeServiceLogUpload 릴리스</span><span class="sxs-lookup"><span data-stu-id="f9d38-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f9d38-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f9d38-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="f9d38-899">Expand, ResourceGroup, InstanceName, InstanceId, Tags, Top on Cmdlet Get-AzureRmConsumptionUsageDetail 등 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="f9d38-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9d38-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9d38-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9d38-901">Export-AzureRmDataLakeStoreChildItemProperties에 대한 예제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f9d38-902">Set-AzureRmDataLakeStoreItemAclEntry에서 재귀 사례에 대한 null 매개 변수 예외 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f9d38-903">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry에 대한 도움말 파일 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f9d38-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9d38-904">AzureRM.Network</span></span>
* <span data-ttu-id="f9d38-905">18.0.0-preview에서 19.0.0-preview로 네트워크 SDK 버전 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f9d38-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f9d38-906">프로토콜 구성을 만들기 위해 추가된 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9d38-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f9d38-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d38-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f9d38-908">기존 Express 경로 회로에 새 회로 연결을 추가하기 위해 추가된 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9d38-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f9d38-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f9d38-910">기존 Express 경로 회로에서 회로 연결을 제거하기 위해 추가된 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9d38-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f9d38-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f9d38-912">회로 연결을 검색하기 위해 추가된 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9d38-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f9d38-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9d38-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9d38-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9d38-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9d38-915">생성된 인증서로 고정 서버 인증 사용(문제 # 5998)</span><span class="sxs-lookup"><span data-stu-id="f9d38-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9d38-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9d38-916">AzureRM.Sql</span></span>
* <span data-ttu-id="f9d38-917">AuditActions 또는 AuditActionGroups를 제거할 수 있도록 업데이트된 감사 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9d38-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f9d38-918">'Azure 복구 서비스 자격 증명 모음을 사용하여 장기 보존 정책을 구성하면 정책이 더 이상 지원되지 않습니다. 새로운 유연 보유 정책으로 요청을 제출하십시오.'라는 메시지와 함께 명령이 실패하는 새로운 유연 보유 정책을 설정할 때</span><span class="sxs-lookup"><span data-stu-id="f9d38-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f9d38-919">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="f9d38-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f9d38-920">Azure SQL Database/ElasticPool Creation/Update 관련 cmdlet을 모두 업데이트하여 규모 및 계층 관련 속성에 대한 SKU 속성을 지원하는 새 데이터베이스 API를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f9d38-921">업데이트된 cmdlet는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f9d38-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f9d38-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9d38-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f9d38-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f9d38-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f9d38-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f9d38-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f9d38-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9d38-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9d38-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9d38-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9d38-928">-Name 매개 변수를 사용할 때 -ResourceGroupName 매개 변수가 필요하도록 'Get-AzureRmTrafficManagerProfile'에 대한 매개 변수를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d38-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
