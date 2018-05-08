---
title: Azure PowerShell 변경 로그 | Microsoft Docs
description: Azure PowerShell에 대한 최신 릴리스의 변경 내용입니다.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 2e80d314991539cb630a0f2a96048bb2e70a05b6
ms.sourcegitcommit: 5f0013981fcea1d689649b9a2b2ffe84ae842e56
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
---
# <a name="release-notes"></a><span data-ttu-id="03e91-103">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="03e91-103">Release notes</span></span>

<span data-ttu-id="03e91-104">Azure PowerShell에 대한 릴리스의 변경 내용 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

# <a name="azure-powershell-570"></a><span data-ttu-id="03e91-105">Azure PowerShell 5.7.0</span><span class="sxs-lookup"><span data-stu-id="03e91-105">Azure PowerShell 5.7.0</span></span>

<span data-ttu-id="03e91-106">Azure PowerShell 5.7.0 설치 관리자: [링크](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)</span><span class="sxs-lookup"><span data-stu-id="03e91-106">Azure PowerShell 5.7.0 Installer: [link](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)</span></span>

<span data-ttu-id="03e91-107">ARM Cmdlet용 갤러리 모듈: [링크](https://www.powershellgallery.com/packages/AzureRM/5.7.0)</span><span class="sxs-lookup"><span data-stu-id="03e91-107">Gallery Module for ARM Cmdlets: [link](https://www.powershellgallery.com/packages/AzureRM/5.7.0)</span></span>

<span data-ttu-id="03e91-108">PowerShell 갤러리에서 `AzureRM`을 설치하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-108">To install `AzureRM` from the PowerShell Gallery, run the following command:</span></span>

```powershell
Install-Module -Name AzureRM -Repository PSGallery -Force
```

<span data-ttu-id="03e91-109">이전 버전의 `AzureRM`에서 업데이트하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-109">To update from an older version of `AzureRM`, run the following command:</span></span>

```powershell
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a><span data-ttu-id="03e91-110">마지막 릴리스 이후 변경 내용</span><span class="sxs-lookup"><span data-stu-id="03e91-110">Changes Since Last Release</span></span>

#### <a name="general"></a><span data-ttu-id="03e91-111">일반</span><span class="sxs-lookup"><span data-stu-id="03e91-111">General</span></span>
* <span data-ttu-id="03e91-112">최신 버전의 Azure ClientRuntime으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="03e91-112">Updated to the latest version of the Azure ClientRuntime</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="03e91-113">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-113">Azure.Storage</span></span>
* <span data-ttu-id="03e91-114">FIPS 정책을 사용하는 컴퓨터에서 Blob 업로드 및 파일 업로드 cmdlet이 실패하는 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-114">Fix the issue that upload Blob and upload File cmdlets fail on FIPS policy enabled machines</span></span>
    - <span data-ttu-id="03e91-115">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="03e91-115">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="03e91-116">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="03e91-116">Set-AzureStorageFileContent</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="03e91-117">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="03e91-117">AzureRM.Billing</span></span>
* <span data-ttu-id="03e91-118">새로운 Cmdlet Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="03e91-118">New Cmdlet Get-AzureRmEnrollmentAccount</span></span>
  - <span data-ttu-id="03e91-119">등록 계정을 검색하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="03e91-119">cmdlet to retrieve enrollment accounts</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="03e91-120">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="03e91-120">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="03e91-121">Cognitive Services Management SDK 버전 4.0.0과 통합됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-121">Integrate with Cognitive Services Management SDK version 4.0.0.</span></span>
* <span data-ttu-id="03e91-122">Get-AzureRmCognitiveServicesAccountUsage 작업을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-122">Add Get-AzureRmCognitiveServicesAccountUsage operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="03e91-123">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-123">AzureRM.Compute</span></span>
* <span data-ttu-id="03e91-124">`Get-AzureRmVmssDiskEncryptionStatus`는 데이터 디스크 수준에서 암호화 상태를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-124">`Get-AzureRmVmssDiskEncryptionStatus` supports encryption status at data disk level</span></span>
* <span data-ttu-id="03e91-125">`Get-AzureRmVmssVmDiskEncryptionStatus`는 데이터 디스크 수준에서 암호화 상태를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-125">`Get-AzureRmVmssVmDiskEncryptionStatus` supports encryption status at data disk level</span></span>
* <span data-ttu-id="03e91-126">영역 복원력에 대한 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-126">Update for Zone Resilient</span></span>
* <span data-ttu-id="03e91-127">'New-AzureRmVm' 및 'New-AzureRmVmss'(간단한 매개 변수 집합)가 가용성 영역을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-127">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support availability zones.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="03e91-128">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="03e91-128">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="03e91-129">Commands.Resources.Rest 및 ARM/Storage SDK에 대한 의존성을 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-129">Decouple reliance on Commands.Resources.Rest and ARM/Storage SDKs.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="03e91-130">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="03e91-130">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="03e91-131">디버그 기능 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-131">Add debug functionality</span></span>
* <span data-ttu-id="03e91-132">ADLS 데이터플레인 SDK 버전을 1.1.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-132">Update the version of the ADLS dataplane SDK to 1.1.2</span></span>
* <span data-ttu-id="03e91-133">Export-AzureRmDataLakeStoreItem - PerFileThreadCount, ConcurrentFileCount 매개 변수가 사용되지 않으며 Concurrency 매개 변수가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-133">Export-AzureRmDataLakeStoreItem - Deprecated parameters PerFileThreadCount, ConcurrentFileCount and introduced parameter Concurrency</span></span>
* <span data-ttu-id="03e91-134">Import-AzureRMDataLakeStoreItem - PerFileThreadCount, ConcurrentFileCount 매개 변수가 사용되지 않으며 Concurrency 매개 변수가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-134">Import-AzureRMDataLakeStoreItem - Deprecated parametersPerFileThreadCount, ConcurrentFileCount and introduced parameter Concurrency</span></span>
* <span data-ttu-id="03e91-135">Get-AzureRMDataLakeStoreItemContent - 4MB를 초과하는 콘텐츠에 대한 말단 동작이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-135">Get-AzureRMDataLakeStoreItemContent - Fixed the tail behavior for contents greater than 4MB</span></span>
* <span data-ttu-id="03e91-136">Set-AzureRMDataLakeStoreItemExpiry - 상대 만료 시간을 설정하는 새로운 매개 변수 집합 SetRelativeExpiry가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-136">Set-AzureRMDataLakeStoreItemExpiry - Introduced new parameter set SetRelativeExpiry for setting relative expiration time</span></span>
* <span data-ttu-id="03e91-137">Remove-AzureRmDataLakeStoreItem - Clean 매개 변수가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-137">Remove-AzureRmDataLakeStoreItem - Deprecated parameter Clean.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="03e91-138">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="03e91-138">AzureRM.EventHub</span></span>
* <span data-ttu-id="03e91-139">New-AzureRmEventHubGeoDRConfiguration의 AlternameName이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-139">Fixed AlternameName in New-AzureRmEventHubGeoDRConfiguration</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="03e91-140">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="03e91-140">AzureRM.KeyVault</span></span>
* <span data-ttu-id="03e91-141">파이핑 시나리오를 포함하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-141">Updated cmdlets to include piping scenarios</span></span>
* <span data-ttu-id="03e91-142">향후 호환성이 손상되는 변경 릴리스에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-142">Add deprecation messages for upcoming breaking change release</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="03e91-143">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="03e91-143">AzureRM.Network</span></span>
* <span data-ttu-id="03e91-144">Network cmdlet 관련 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-144">Fix error message with Network cmdlets</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="03e91-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="03e91-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="03e91-146">customproperties를 지원하기 위해 Rules의 CorrelationFilter에 'properties'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-146">Added 'properties' in CorrelationFilter of Rules to support customproperties</span></span>
* <span data-ttu-id="03e91-147">New-AzureRmServiceBusGeoDRConfiguration 도움말이 업데이트되고 Rules cmdlet 출력이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-147">updated New-AzureRmServiceBusGeoDRConfiguration help and fixed Rules cmdlet output</span></span>
* <span data-ttu-id="03e91-148">New-AzureRmServiceBusQueue 및 New-AzureRmServiceBusSubscription cmdlet의 auto-forward 속성이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-148">Fixed auto-forward properties in New-AzureRmServiceBusQueue and New-AzureRmServiceBusSubscription cmdlet</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="03e91-149">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="03e91-149">AzureRM.Sql</span></span>
* <span data-ttu-id="03e91-150">탄력적 풀에서 비동기 작업의 취소를 지원하기 위해 새로운 cmdlet 'Stop-AzureRmSqlElasticPoolActivity' 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-150">Add new cmdlet 'Stop-AzureRmSqlElasticPoolActivity' to support canceling the asynchronous operations on elastic pool</span></span>
* <span data-ttu-id="03e91-151">자세한 정보를 반영하도록 Get-AzureRmSqlDatabaseActivity 및 Get-AzureRmSqlElasticPoolActivity cmdlet에 대한 응답 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-151">Update the response for cmdlets Get-AzureRmSqlDatabaseActivity and Get-AzureRmSqlElasticPoolActivity to reflect more information in the response</span></span>

<span data-ttu-id="03e91-152">마지막 릴리스 이후 변경 내용: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018</span><span class="sxs-lookup"><span data-stu-id="03e91-152">Changes since last release: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018</span></span>

## <a name="560---march-2018"></a><span data-ttu-id="03e91-153">5.6.0 - 2018년 3월</span><span class="sxs-lookup"><span data-stu-id="03e91-153">5.6.0 - March 2018</span></span>

#### <a name="general"></a><span data-ttu-id="03e91-154">일반</span><span class="sxs-lookup"><span data-stu-id="03e91-154">General</span></span>
* <span data-ttu-id="03e91-155">CloudShell의 기본 리소스 그룹 문제 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-155">Fix issue with Default Resource Group in CloudShell</span></span>
* <span data-ttu-id="03e91-156">모듈 가져오는 중에 잘못된 시작 스크립트가 실행되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-156">Fix issue where incorrect startup scripts were being executed during module import</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="03e91-157">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="03e91-157">AzureRM.Profile</span></span>
* <span data-ttu-id="03e91-158">지원되지 않는 시나리오에서 MSI 인증 사용</span><span class="sxs-lookup"><span data-stu-id="03e91-158">Enable MSI authentication in unsupported scenarios</span></span>
* <span data-ttu-id="03e91-159">사용자 정의 관리 서비스 ID 지원 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-159">Add support for user-defined Managed Service Identity</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="03e91-160">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="03e91-160">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="03e91-161">빌드 시 스크립트 정리 문제 수정됨</span><span class="sxs-lookup"><span data-stu-id="03e91-161">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="03e91-162">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="03e91-162">AzureRM.Cdn</span></span>
* <span data-ttu-id="03e91-163">빌드 시 스크립트 정리 문제 수정됨</span><span class="sxs-lookup"><span data-stu-id="03e91-163">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="03e91-164">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-164">AzureRM.Compute</span></span>
* <span data-ttu-id="03e91-165">'New-AzureRmVM' 및 'New-AzureRmVMSS'가 데이터 디스크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-165">'New-AzureRmVM' and 'New-AzureRmVMSS' support data disks.</span></span>
* <span data-ttu-id="03e91-166">'New-AzureRmVM' 및 'New-AzureRmVMSS'가 이름별 또는 ID별로 사용자 지정 이미지를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-166">'New-AzureRmVM' and 'New-AzureRmVMSS' support custom image by name or by id.</span></span>
* <span data-ttu-id="03e91-167">로그 분석 기능</span><span class="sxs-lookup"><span data-stu-id="03e91-167">Log analytic feature</span></span>
    - <span data-ttu-id="03e91-168">'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-168">Added 'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet</span></span>
    - <span data-ttu-id="03e91-169">'Export-AzureRmLogAnalyticThrottledRequests' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-169">Added 'Export-AzureRmLogAnalyticThrottledRequests' cmdlet</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="03e91-170">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="03e91-170">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="03e91-171">컨테이너 레지스트리 및 Azure 파일 볼륨 마운트에 대한 매개 변수 세트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-171">Fix parameter sets issue for container registry and azure file volume mount</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="03e91-172">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="03e91-172">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="03e91-173">ADF .Net SDK를 다음과 같은 변경 사항이 포함된 버전 0.6.0-preview로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-173">Updated the ADF .Net SDK to version 0.6.0-preview containing the following changes:</span></span>
    - <span data-ttu-id="03e91-174">새로운 AzureDatabricks LinkedService 및 DatabricksNotebook Activity 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-174">Added new AzureDatabricks LinkedService and DatabricksNotebook Activity</span></span>
    - <span data-ttu-id="03e91-175">HDInsightOnDemand LinkedService의 headNodeSize 및 dataNodeSize 속성 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-175">Added headNodeSize and dataNodeSize properties in HDInsightOnDemand LinkedService</span></span>
    - <span data-ttu-id="03e91-176">SalesforceMarketingCloud에 대한 LinkedService, Dataset, CopySource 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-176">Added LinkedService, Dataset, CopySource for SalesforceMarketingCloud</span></span>
    - <span data-ttu-id="03e91-177">모든 작업에서 SecureOutput에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-177">Added support for SecureOutput on all activities</span></span>
    - <span data-ttu-id="03e91-178">ForEach 작업에서 실행될 동시 작업 수를 제어하는 새로운 BatchCount 속성 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-178">Added new BatchCount property on ForEach activity which control how many concurrent activities to run</span></span>
    - <span data-ttu-id="03e91-179">새 필터 작업 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-179">Added new Filter Activity</span></span>
    - <span data-ttu-id="03e91-180">연결된 서비스 매개 변수 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-180">Added Linked Service Parameters support</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="03e91-181">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="03e91-181">AzureRM.Dns</span></span>
* <span data-ttu-id="03e91-182">사설 DNS 영역 지원(공개 미리 보기)</span><span class="sxs-lookup"><span data-stu-id="03e91-182">Support for Private DNS Zones (Public Preview)</span></span>
    - <span data-ttu-id="03e91-183">연결된 가상 네트워크에만 표시되는 DNS 영역을 만들 수있는 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-183">Adds ability to create DNS zones that are visible only to the associated virtual networks</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="03e91-184">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="03e91-184">AzureRM.Network</span></span>
* <span data-ttu-id="03e91-185">DNS cmdlet과의 호환성을 위해 모델 형식 업데이트.</span><span class="sxs-lookup"><span data-stu-id="03e91-185">Updating model types for compatibility with DNS cmdlets.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="03e91-186">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-186">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="03e91-187">ASR Azure-Azure Site Recovery에 대한 변경 사항(cmdlet은 현재 Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure, VMware - Azure에 대한 작업을 지원)</span><span class="sxs-lookup"><span data-stu-id="03e91-187">Changes for ASR Azure to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure,VMware to Azure)</span></span>
    - <span data-ttu-id="03e91-188">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="03e91-188">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="03e91-189">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="03e91-189">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>
    - <span data-ttu-id="03e91-190">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="03e91-190">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="03e91-191">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="03e91-191">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="03e91-192">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-192">AzureRM.Storage</span></span>
* <span data-ttu-id="03e91-193">new 및 set Storage Account cmdlet에서 Encryption at Rest는 기본적으로 활성화되며 비활성화할 수 없으므로 EnableEncryptionService 및 DisableEncryptionService 같은 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="03e91-193">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="03e91-194">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03e91-194">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="03e91-195">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03e91-195">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="03e91-196">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="03e91-196">AzureRM.Websites</span></span>
* <span data-ttu-id="03e91-197">Remove-AzureRmWebAppSlot에 대한 도움말 수정됨</span><span class="sxs-lookup"><span data-stu-id="03e91-197">Fixed the help for Remove-AzureRmWebAppSlot</span></span>

## <a name="550---march-2018"></a><span data-ttu-id="03e91-198">5.5.0 - 2018년 3월</span><span class="sxs-lookup"><span data-stu-id="03e91-198">5.5.0 - March 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="03e91-199">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="03e91-199">AzureRM.Profile</span></span>
* <span data-ttu-id="03e91-200">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-200">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="03e91-201">6.0.8 버전과 병렬로 Newtonsoft.Json 버전 10.0.3 로드</span><span class="sxs-lookup"><span data-stu-id="03e91-201">Load version 10.0.3 of Newtonsoft.Json side-by-side with version 6.0.8</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="03e91-202">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-202">Azure.Storage</span></span>
* <span data-ttu-id="03e91-203">일시 삭제 기능 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-203">Support Soft-Delete feature</span></span>
    - <span data-ttu-id="03e91-204">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="03e91-204">Enable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="03e91-205">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="03e91-205">Disable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="03e91-206">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="03e91-206">Get-AzureStorageBlob</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="03e91-207">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="03e91-207">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="03e91-208">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-208">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="03e91-209">2017-08-01 API 버전 지원 및 방화벽과 쿼리 스케일 아웃 기능 지원 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-209">Add support of firewall and query scaleout feature, as well as support of 2017-08-01 api version.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="03e91-210">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="03e91-210">AzureRM.Automation</span></span>
* <span data-ttu-id="03e91-211">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-211">Fixed issue with importing aliases</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="03e91-212">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="03e91-212">AzureRM.Cdn</span></span>
* <span data-ttu-id="03e91-213">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-213">Fixed issue with importing aliases</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="03e91-214">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="03e91-214">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="03e91-215">notice.txt 및 알림 메시지 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-215">Update notice.txt and notice message.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="03e91-216">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-216">AzureRM.Compute</span></span>
* <span data-ttu-id="03e91-217">'New-AzureRmVMSS'가 자세한 정보 표시 모드로 연결 문자열 인쇄</span><span class="sxs-lookup"><span data-stu-id="03e91-217">'New-AzureRmVMSS' prints connection strings in verbose mode.</span></span>
* <span data-ttu-id="03e91-218">'New-AzureRmVmss'가 공용 IP 주소, 부하 분산 규칙, 인바운드 NAT 규칙 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-218">'New-AzureRmVmss' supports public IP address, load balancing rules, inbound NAT rules.</span></span>
* <span data-ttu-id="03e91-219">WriteAccelerator 기능</span><span class="sxs-lookup"><span data-stu-id="03e91-219">WriteAccelerator feature</span></span>
    - <span data-ttu-id="03e91-220">WriteAccelerator 스위치 매개 변수가 다음 cmdlets에 추가됨: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="03e91-220">Added WriteAccelerator switch parameter to the following cmdlets: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span></span>
    - <span data-ttu-id="03e91-221">OsDiskWriteAccelerator 스위치 매개 변수가 다음 cmdlet에 추가됨:   Set-AzureRmVmssStorageProfile.</span><span class="sxs-lookup"><span data-stu-id="03e91-221">Added OsDiskWriteAccelerator switch parameter to the following cmdlet:     Set-AzureRmVmssStorageProfile.</span></span>
    - <span data-ttu-id="03e91-222">OsDiskWriteAccelerator 부울 매개 변수가 다음 cmdlet에 추가됨:     Update-AzureRmVM     Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="03e91-222">Added OsDiskWriteAccelerator Boolean parameter to the following cmdlets:     Update-AzureRmVM     Update-AzureRmVmss</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="03e91-223">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="03e91-223">AzureRM.DataFactories</span></span>
* <span data-ttu-id="03e91-224">일부 암호화 작업에 대해 의미 없는 오류를 일으키는 자격 증명 암호화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-224">Fix credential encryption issue that caused no meaningful error for some encryption operations</span></span>
* <span data-ttu-id="03e91-225">데이터 팩터리 전체에서 공유 가능하도록 통합 런타임 활성화</span><span class="sxs-lookup"><span data-stu-id="03e91-225">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="03e91-226">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="03e91-226">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="03e91-227">"Set-AzureRmDataFactoryV2IntegrationRuntime" cmd용 매개 변수 "SetupScriptContainerSasUri" 및 "Edition"을 추가하여 사용자 지정 설치 및 버전 선택 기능 활성화</span><span class="sxs-lookup"><span data-stu-id="03e91-227">Add parameter "SetupScriptContainerSasUri" and "Edition" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable custom setup and edition selection functionality</span></span>
* <span data-ttu-id="03e91-228">일부 암호화 작업에 대해 의미 없는 오류를 일으키는 자격 증명 암호화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-228">Fix credential encryption issue that caused no meaningful error for some encryption operations.</span></span>
* <span data-ttu-id="03e91-229">데이터 팩터리 전체에서 공유 가능하도록 통합 런타임 활성화</span><span class="sxs-lookup"><span data-stu-id="03e91-229">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="03e91-230">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="03e91-230">AzureRM.HDInsight</span></span>
* <span data-ttu-id="03e91-231">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-231">Fixed issue with importing aliases</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="03e91-232">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="03e91-232">AzureRM.KeyVault</span></span>
* <span data-ttu-id="03e91-233">Set-AzureRmKeyVaultAccessPolicy용 예제 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-233">Fixed example for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="03e91-234">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="03e91-234">AzureRM.Network</span></span>
* <span data-ttu-id="03e91-235">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-235">Fixed issue with importing aliases</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="03e91-236">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-236">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="03e91-237">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-237">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="03e91-238">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03e91-238">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="03e91-239">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-239">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="03e91-240">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-240">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="03e91-241">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-241">Fixed issue with importing aliases</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="03e91-242">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="03e91-242">AzureRM.Resources</span></span>
* <span data-ttu-id="03e91-243">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-243">Fixed issue with importing aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="03e91-244">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="03e91-244">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="03e91-245">큐에 EnableBatchedOperations 속성 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-245">Added EnableBatchedOperations property to Queue</span></span>
* <span data-ttu-id="03e91-246">구독에 DeadLetteringOnFilterEvaluationExceptions 속성 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-246">Added DeadLetteringOnFilterEvaluationExceptions property to Subscriptions</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="03e91-247">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="03e91-247">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="03e91-248">Service Fabric cmdlet 새로 고침</span><span class="sxs-lookup"><span data-stu-id="03e91-248">Service Fabric cmdlet refresh</span></span>
  - <span data-ttu-id="03e91-249">ARM 템플릿 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="03e91-249">Updated ARM templates</span></span>
  - <span data-ttu-id="03e91-250">실패한 작업이 더 이상 롤백되지 않음</span><span class="sxs-lookup"><span data-stu-id="03e91-250">Failed operations no longer rollback</span></span>
  - <span data-ttu-id="03e91-251">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="03e91-251">Add-AzureRmServiceFabricNodeType</span></span>
    - <span data-ttu-id="03e91-252">관리 디스크에 대한 VM 기본값</span><span class="sxs-lookup"><span data-stu-id="03e91-252">VMs default to managed disks</span></span>
    - <span data-ttu-id="03e91-253">기존 VMSS 서브넷 사용됨</span><span class="sxs-lookup"><span data-stu-id="03e91-253">Existing VMSS subnet used</span></span>
    - <span data-ttu-id="03e91-254">모든 작업은 idempotent임</span><span class="sxs-lookup"><span data-stu-id="03e91-254">All operations are idempotent</span></span>
  - <span data-ttu-id="03e91-255">Remove-AzureRmServiceFabricNodeType 정리가 부분적으로 VMSS 및/또는 클러스터 노드 유형 생성</span><span class="sxs-lookup"><span data-stu-id="03e91-255">Remove-AzureRmServiceFabricNodeType cleans up partially created VMSS and/or cluster node types</span></span>
  - <span data-ttu-id="03e91-256">복합 속성 유형에 대한 PSCluster 개체의 출력 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-256">Fixed output of PSCluster object for complex property types</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="03e91-257">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="03e91-257">AzureRM.Sql</span></span>
* <span data-ttu-id="03e91-258">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-258">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="03e91-259">Get-AzureRmSqlServer, New-AzureRmSqlServer 및 Remove-AzureRmSqlServer 응답이 FullyQualifiedDomainName 속성에 포함됨.</span><span class="sxs-lookup"><span data-stu-id="03e91-259">Get-AzureRmSqlServer, New-AzureRmSqlServer, and Remove-AzureRmSqlServer response now includes FullyQualifiedDomainName property.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="03e91-260">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="03e91-260">AzureRM.Websites</span></span>
* <span data-ttu-id="03e91-261">별칭 가져오기 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-261">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="03e91-262">New-AzureRMWebApp - 로컬 Git 리포지토리 지원과 함께 간소화된 WebApp 생성을 위한 매개 변수 집합이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-262">New-AzureRMWebApp - added parameter set for simplified WebApp creation, with local git repository support.</span></span>

## <a name="540---february-2018"></a><span data-ttu-id="03e91-263">5.4.0 - 2018년 2월</span><span class="sxs-lookup"><span data-stu-id="03e91-263">5.4.0 - February 2018</span></span>
#### <a name="azurermautomation"></a><span data-ttu-id="03e91-264">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="03e91-264">AzureRM.Automation</span></span>
* <span data-ttu-id="03e91-265">New-AzureRmAutomationModule의 별칭이 Import-AzureRmAutomationModule에 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-265">Added alias from New-AzureRmAutomationModule to Import-AzureRmAutomationModule</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="03e91-266">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-266">AzureRM.Compute</span></span>
* <span data-ttu-id="03e91-267">일부 Get cmdlet에 대한 ErrorAction 문제 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-267">Fix ErrorAction issue for some of Get cmdlets.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="03e91-268">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="03e91-268">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="03e91-269">Azure Container Instance SDK 2018-02-01 적용</span><span class="sxs-lookup"><span data-stu-id="03e91-269">Apply Azure Container Instance SDK 2018-02-01</span></span>
    - <span data-ttu-id="03e91-270">DNS 이름 레이블 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-270">Support DNS name label</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="03e91-271">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="03e91-271">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="03e91-272">이전에 작동하지 않았던 모든 GET cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-272">Fixed all of the GET cmdlets which previously weren't working.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="03e91-273">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="03e91-273">AzureRM.EventHub</span></span>
* <span data-ttu-id="03e91-274">Get-AzureRmEventHubGeoDRConfiguration 도움말의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-274">Fix bug in Get-AzureRmEventHubGeoDRConfiguration help</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="03e91-275">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="03e91-275">AzureRM.Network</span></span>
* <span data-ttu-id="03e91-276">새 연결 모니터를 만드는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-276">Added cmdlet to create a new connection monitor</span></span>
    - <span data-ttu-id="03e91-277">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03e91-277">New-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="03e91-278">연결 모니터를 업데이트하는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-278">Added cmdlet to update a connection monitor</span></span>
    - <span data-ttu-id="03e91-279">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03e91-279">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="03e91-280">연결 모니터 또는 연결 모니터 목록을 가져오는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-280">Added cmdlet to get connection monitor or connection monitor list</span></span>
    - <span data-ttu-id="03e91-281">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03e91-281">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="03e91-282">연결 모니터를 쿼리하는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-282">Added cmdlet to query connection monitor</span></span>
    - <span data-ttu-id="03e91-283">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="03e91-283">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>
* <span data-ttu-id="03e91-284">연결 모니터를 시작하는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-284">Added cmdlet to start connection monitor</span></span>
    - <span data-ttu-id="03e91-285">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03e91-285">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="03e91-286">연결 모니터를 중지하는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-286">Added cmdlet to stop connection monitor</span></span>
    - <span data-ttu-id="03e91-287">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03e91-287">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="03e91-288">연결 모니터를 제거하는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-288">Added cmdlet to remove connection monitor</span></span>
    - <span data-ttu-id="03e91-289">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03e91-289">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="03e91-290">사용되지 않는 예제를 제거하기 위해 Set-AzureRmApplicationGatewayBackendAddressPool 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="03e91-290">Updated Set-AzureRmApplicationGatewayBackendAddressPool documentation to remove deprecated example</span></span>
* <span data-ttu-id="03e91-291">Application Gateway에 EnableHttp2 플래그가 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-291">Added EnableHttp2 flag to Application Gateway</span></span>
    - <span data-ttu-id="03e91-292">New-AzureRmApplicationGateway가 업데이트됨: 선택적 매개 변수 -EnableHttp2가 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-292">Updated New-AzureRmApplicationGateway: Added optional parameter -EnableHttp2</span></span>
* <span data-ttu-id="03e91-293">PublicIpAddress에 IpTags 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-293">Add IpTags to PublicIpAddress</span></span>
    - <span data-ttu-id="03e91-294">New-AzureRmPublicIpAddress가 업데이트됨: IpTags가 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-294">Updated New-AzureRmPublicIpAddress: Added IpTags</span></span>
    - <span data-ttu-id="03e91-295">Iptag를 추가하는 New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="03e91-295">New-AzureRmPublicIpTag to add Iptag</span></span>
* <span data-ttu-id="03e91-296">RouteTable 및 effectiveRoute에 DisableBgpRoutePropagation 속성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-296">Add DisableBgpRoutePropagation property in RouteTable and effectiveRoute.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="03e91-297">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="03e91-297">AzureRM.Resources</span></span>
* <span data-ttu-id="03e91-298">Register-AzureRmProviderFeature: 문서에 누락된 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-298">Register-AzureRmProviderFeature: Added missing example in the docs</span></span>
* <span data-ttu-id="03e91-299">Register-AzureRmResourceProvider: 문서에 누락된 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-299">Register-AzureRmResourceProvider: Added missing example in the docs</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="03e91-300">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-300">AzureRM.Storage</span></span>
* <span data-ttu-id="03e91-301">new 및 set Storage Account cmdlet에서 Encryption at Rest는 기본적으로 활성화되며 비활성화할 수 없으므로 EnableEncryptionService 및 DisableEncryptionService 같은 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="03e91-301">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="03e91-302">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03e91-302">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="03e91-303">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03e91-303">Set-AzureRmStorageAccount</span></span>


## <a name="530---february-2018"></a><span data-ttu-id="03e91-304">5.3.0 - 2018년 2월</span><span class="sxs-lookup"><span data-stu-id="03e91-304">5.3.0 - February 2018</span></span>
### <a name="azurermprofile"></a><span data-ttu-id="03e91-305">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="03e91-305">AzureRM.Profile</span></span>
* <span data-ttu-id="03e91-306">PowerShell 3 및 4에 대한 사용 중단 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-306">Added deprecation warning for PowerShell 3 and 4</span></span>
* <span data-ttu-id="03e91-307">`Add-AzureRmAccount`는 `Connect-AzureRmAccount`로 이름이 변경되었습니다. 이전 cmdlet 이름에 대한 별칭이 추가되었고 다른 별칭(`Login-AzAccount` 및 `Login-AzureRmAccount`)이 새 cmdlet 이름으로 리디렉션되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-307">`Add-AzureRmAccount` has been renamed as `Connect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Login-AzAccount` and `Login-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="03e91-308">`Remove-AzureRmAccount`는 `Disconnect-AzureRmAccount`로 이름이 변경되었습니다. 이전 cmdlet 이름에 대한 별칭이 추가되었고 다른 별칭(`Logout-AzAccount` 및 `Logout-AzureRmAccount`)이 새 cmdlet 이름으로 리디렉션되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-308">`Remove-AzureRmAccount` has been renamed as `Disconnect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Logout-AzAccount` and `Logout-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="03e91-309">`Login-AzureRmAccount` 대신 `Connect-AzureRmAccount`를 사용하도록 리소스 문자열이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-309">Corrected Resource Strings to use `Connect-AzureRmAccount` instead of `Login-AzureRmAccount`</span></span>
* <span data-ttu-id="03e91-310">`Add-AzureRmEnvironment` 및 `Set-AzureRmEnvironment`</span><span class="sxs-lookup"><span data-stu-id="03e91-310">`Add-AzureRmEnvironment` and `Set-AzureRmEnvironment`</span></span>
  - <span data-ttu-id="03e91-311">OperationalInsights 데이터 평면 RP와 함께 사용할 매개 변수로 `-AzureOperationalInsightsEndpoint` 및 `-AzureOperationalInsightsEndpointResourceId`가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-311">Added `-AzureOperationalInsightsEndpoint` and `-AzureOperationalInsightsEndpointResourceId` as parameters for use with OperationalInsights data plane RP.</span></span>

### <a name="azurermanalysisservices"></a><span data-ttu-id="03e91-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="03e91-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="03e91-313">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-313">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="03e91-314">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-314">AzureRM.Compute</span></span>
* <span data-ttu-id="03e91-315">간소화된 매개 변수 집합 `New-AzureRmVM`에 `-AvailabilitySetName` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-315">Added `-AvailabilitySetName` parameter to the simplified parameterset of `New-AzureRmVM`.</span></span>
* <span data-ttu-id="03e91-316">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-316">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="03e91-317">VM 및 VM 확장 집합에 대한 사용자 할당 ID가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-317">User assigned identity support for VM and VM scale set</span></span>
    - <span data-ttu-id="03e91-318">`New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM`, `Update-AzureRmVmss`에 `-IdentityType` 및 `-IdentityId` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-318">`-IdentityType` and `-IdentityId` parameters are added to `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` and `Update-AzureRmVmss`</span></span>
* <span data-ttu-id="03e91-319">`-EnableIPForwarding` 매개 변수가 `Add-AzureRmVmssNetworkInterfaceConfig`에 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-319">Added `-EnableIPForwarding` parameter to `Add-AzureRmVmssNetworkInterfaceConfig`</span></span>
* <span data-ttu-id="03e91-320">`-Priority` 매개 변수가 `New-AzureRmVmssConfig`에 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-320">Added `-Priority` parameter to `New-AzureRmVmssConfig`</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="03e91-321">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="03e91-321">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="03e91-322">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-322">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="03e91-323">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="03e91-323">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="03e91-324">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-324">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="03e91-325">`Login-AzureRmAccount`를 사용하여 로그인하지 않고 이 cmdlet을 실행하는 경우 오류 메시지 `Test-AzureRmDataLakeStoreAccount`가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-325">Corrected the error message of `Test-AzureRmDataLakeStoreAccount` when running this cmdlet without having logged in with `Login-AzureRmAccount`</span></span>

### <a name="azurermeventgrid"></a><span data-ttu-id="03e91-326">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="03e91-326">AzureRM.EventGrid</span></span>
* <span data-ttu-id="03e91-327">2018-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-327">Updated to use the 2018-01-01 API version.</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="03e91-328">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="03e91-328">AzureRM.EventHub</span></span>

* <span data-ttu-id="03e91-329">지역 재해 복구 작업에 대한 아래의 새 명령이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-329">Added below new commands for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="03e91-330">새 별칭(재해 복구 구성)을 만드는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-330">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="03e91-331">새 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-331">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="03e91-332">재해 복구를 사용하지 않고 기본 네임스페이스에서 보조 네임스페이스로의 변경 사항 복제 중지</span><span class="sxs-lookup"><span data-stu-id="03e91-332">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - <span data-ttu-id="03e91-333">재해 복구 장애 조치(failover)를 호출하고 별칭이 보조 네임스페이스를 가리키도록 다시 구성</span><span class="sxs-lookup"><span data-stu-id="03e91-333">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - <span data-ttu-id="03e91-334">별칭 삭제(재해 복구 구성)</span><span class="sxs-lookup"><span data-stu-id="03e91-334">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* <span data-ttu-id="03e91-335">네임스페이스 이름 및 GeoDr 구성 이름 - 별칭 가용성을 검사하는 아래의 새 명령이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-335">Added below new commands for checking the Namespace Name and GeoDr Configuration Name - Alias availability.</span></span>
  - <span data-ttu-id="03e91-336">네임스페이스 이름의 가용성 이름 또는 별칭(재해 복구 구성) 이름을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-336">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a><span data-ttu-id="03e91-337">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="03e91-337">AzureRM.Insights</span></span>
* <span data-ttu-id="03e91-338">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-338">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="03e91-339">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="03e91-339">AzureRM.KeyVault</span></span>
* <span data-ttu-id="03e91-340">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-340">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="03e91-341">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="03e91-341">AzureRM.Network</span></span>
* <span data-ttu-id="03e91-342">'리소스를 덮어쓰시겠습니까?'라는 덮어쓰기 메시지가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-342">Fix overwrite message 'Are you sure you want to overwriteresource'</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="03e91-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="03e91-344">`Invoke-AzureRmOperationalInsightsQuery`를 통해 V2 API 쿼리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-344">Added support for V2 API querying via `Invoke-AzureRmOperationalInsightsQuery`.</span></span> <span data-ttu-id="03e91-345">새로운 API에 대한 보다 자세한 내용은 [https://dev.loganalytics.io/](https://dev.loganalytics.io/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-345">See [https://dev.loganalytics.io/](https://dev.loganalytics.io/) for more info on the new API.</span></span>

### <a name="azurermresources"></a><span data-ttu-id="03e91-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="03e91-346">AzureRM.Resources</span></span>
* <span data-ttu-id="03e91-347">`Get-AzureRmADServicePrincipal`: SPN 매개 변수 설정과 중복되는 기본 빈 매개 변수 설정에서 `-ServicePrincipalName`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-347">`Get-AzureRmADServicePrincipal`: Removed `-ServicePrincipalName` from the default Empty parameter set as it was redundant with the SPN parameter set</span></span>

### <a name="azurermservicebus"></a><span data-ttu-id="03e91-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="03e91-348">AzureRM.ServiceBus</span></span>

* <span data-ttu-id="03e91-349">`Remove-AzureRmServiceBusRule` 및 `Get-AzureRmServiceBusKey`에 대한 기능 수정이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-349">Added functionality fix for `Remove-AzureRmServiceBusRule` and `Get-AzureRmServiceBusKey`</span></span>
* <span data-ttu-id="03e91-350">지역 재해 복구 작업에 대한 아래의 새 commandlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-350">Added below new commandlets for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="03e91-351">새 별칭(재해 복구 구성)을 만드는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-351">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="03e91-352">새 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-352">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="03e91-353">재해 복구를 사용하지 않고 기본 네임스페이스에서 보조 네임스페이스로의 변경 사항 복제 중지</span><span class="sxs-lookup"><span data-stu-id="03e91-353">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - <span data-ttu-id="03e91-354">재해 복구 장애 조치(failover)를 호출하고 별칭이 보조 네임스페이스를 가리키도록 다시 구성</span><span class="sxs-lookup"><span data-stu-id="03e91-354">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - <span data-ttu-id="03e91-355">별칭 삭제(재해 복구 구성)</span><span class="sxs-lookup"><span data-stu-id="03e91-355">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmServiceBusDRConfigurations`
* <span data-ttu-id="03e91-356">지역 재해 복구 - 별칭 이름 확인 가용성 작업을 지원하도록 `Test-AzureRmServiceBusName` commandlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-356">Updated `Test-AzureRmServiceBusName` commandlets to support Geo Disaster Recovery - Alias name check availability operations.</span></span>
  - <span data-ttu-id="03e91-357">네임스페이스 이름의 가용성 이름 또는 별칭(재해 복구 구성) 이름을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-357">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a><span data-ttu-id="03e91-358">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="03e91-358">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="03e91-359">`Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-359">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

## <a name="520---january-2018"></a><span data-ttu-id="03e91-360">5.2.0 - 2018년 1월</span><span class="sxs-lookup"><span data-stu-id="03e91-360">5.2.0 - January 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="03e91-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="03e91-361">AzureRM.Profile</span></span>
* <span data-ttu-id="03e91-362">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-362">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-363">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="03e91-363">Add-AzureRmAccount</span></span>
  * <span data-ttu-id="03e91-364">현재 VM/서비스에 있는 관리 서비스 ID의 자격 증명을 사용하여 인증하기 위해 -MSI 로그인을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-364">Added -MSI login for authenticationg using the credentials of the Managed Service Identity of the current VM / Service</span></span>
  * <span data-ttu-id="03e91-365">사용자 제공 액세스 토큰을 사용하여 로그인할 때 KeyVault 인증을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-365">Fixed KeyVault Authentication when logging in with user-provided access tokens</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="03e91-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-366">Azure.Storage</span></span>
* <span data-ttu-id="03e91-367">Storage 서비스 속성을 가져오고 설정하는 cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-367">Add cmdlets to get and set Storage service properties</span></span>
    - <span data-ttu-id="03e91-368">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="03e91-368">Get-AzureStorageServiceProperty</span></span>
    - <span data-ttu-id="03e91-369">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="03e91-369">Update-AzureStorageServiceProperty</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="03e91-370">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="03e91-370">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="03e91-371">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-371">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="03e91-372">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="03e91-372">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="03e91-373">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-373">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-374">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-374">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-375">New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty 및 New-AzureRmApiManagement에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-375">Obsoleted -Tags in favor of -Tag for New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty, and New-AzureRmApiManagement</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="03e91-376">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-376">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="03e91-377">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-377">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-378">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-378">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="03e91-379">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="03e91-379">AzureRM.Automation</span></span>
* <span data-ttu-id="03e91-380">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-380">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-381">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-381">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-382">Set-AzureRmAutomationRunbook에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-382">Obsoleted -Tags in favor of -Tag for Set-AzureRmAutomationRunbook</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="03e91-383">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-383">AzureRM.Backup</span></span>
* <span data-ttu-id="03e91-384">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-384">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-385">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-385">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="03e91-386">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-386">AzureRM.Batch</span></span>
* <span data-ttu-id="03e91-387">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-387">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-388">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-388">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="03e91-389">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="03e91-389">AzureRM.Cdn</span></span>
* <span data-ttu-id="03e91-390">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-390">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-391">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-391">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-392">New-AzureRmCdnEndpoint 및 New-AzureRmCdnProfile에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-392">Obsoleted -Tags in favor of -Tag for New-AzureRmCdnEndpoint and New-AzureRmCdnProfile</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="03e91-393">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="03e91-393">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="03e91-394">Cognitive Services Management SDK 버전 3.0.0과 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-394">Integrate with Cognitive Services Management SDK version 3.0.0.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="03e91-395">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-395">AzureRM.Compute</span></span>
* <span data-ttu-id="03e91-396">New-AzureRmVmss에 간소화된 매개 변수 집합이 추가되었습니다. 따라서 스마트 기본값을 사용하여 Virtual Machine Scale Set과 필요한 모든 리소스가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-396">Added simplified parameter set to New-AzureRmVmss, which creates a Virtual Machine Scale Set and all required resources using smart defaults</span></span>
* <span data-ttu-id="03e91-397">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-397">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-398">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-398">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-399">New-AzureRmVm 및 Update-AzureRmVm에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-399">Obsoleted -Tags in favor of -Tag for New-AzureRmVm and Update-AzureRmVm</span></span>
* <span data-ttu-id="03e91-400">영역이 제한에 포함될 때 Get-AzureRmComputeResourceSku cmdlet을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-400">Fixed Get-AzureRmComputeResourceSku cmdlet when Zone is included in restriction.</span></span>
* <span data-ttu-id="03e91-401">Azure Monitor 동기화 지원을 위해 진단 에이전트 구성 스키마를 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-401">Updated Diagnostics Agent configuration schema for Azure Monitor sink support.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="03e91-402">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="03e91-402">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="03e91-403">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-403">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-404">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-404">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="03e91-405">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="03e91-405">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="03e91-406">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-406">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-407">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-407">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="03e91-408">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="03e91-408">AzureRM.DataFactories</span></span>
* <span data-ttu-id="03e91-409">모든 데이터 저장소 연결 서비스에 대해 Azure Key Vault 지원을 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-409">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="03e91-410">Azure SSIS 통합 런타임에 라이선스 형식 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-410">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="03e91-411">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-411">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-412">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-412">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-413">New-AzureRmDataFactory에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-413">Obsoleted -Tags in favor of -Tag for New-AzureRmDataFactory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="03e91-414">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="03e91-414">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="03e91-415">모든 데이터 저장소 연결 서비스에 대해 Azure Key Vault 지원을 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-415">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="03e91-416">Azure SSIS 통합 런타임에 라이선스 형식 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-416">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="03e91-417">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-417">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-418">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-418">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-419">AHUB 기능을 사용하도록 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd에 "LicenseType" 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-419">Add parameter "LicenseType" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable AHUB functionality</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="03e91-420">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="03e91-420">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="03e91-421">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-421">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-422">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-422">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-423">New-AzureRmDataLakeAnalyticsAccount 및 Set-AzureRmDataLakeAnalyticsAccount에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-423">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeAnalyticsAccount and Set-AzureRmDataLakeAnalyticsAccount</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="03e91-424">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="03e91-424">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="03e91-425">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-425">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-426">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-426">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-427">New-AzureRmDataLakeStoreAccount 및 Set-AzureRmDataLakeStoreAccount에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-427">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeStoreAccount and Set-AzureRmDataLakeStoreAccount</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="03e91-428">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="03e91-428">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="03e91-429">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-429">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="03e91-430">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="03e91-430">AzureRM.Dns</span></span>
* <span data-ttu-id="03e91-431">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-431">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="03e91-432">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="03e91-432">AzureRM.EventGrid</span></span>
* <span data-ttu-id="03e91-433">다음과 같은 새 cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-433">Added the following new cmdlet:</span></span>
  - <span data-ttu-id="03e91-434">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="03e91-434">Update-AzureRmEventGridSubscription</span></span>
    - <span data-ttu-id="03e91-435">Event Grid 이벤트 구독의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-435">Update the properties of an Event Grid event subscription.</span></span>
* <span data-ttu-id="03e91-436">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-436">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-437">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-437">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="03e91-438">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="03e91-438">AzureRM.EventHub</span></span>
* <span data-ttu-id="03e91-439">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-439">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-440">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-440">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="03e91-441">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="03e91-441">AzureRM.HDInsight</span></span>
* <span data-ttu-id="03e91-442">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-442">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-443">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-443">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="03e91-444">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="03e91-444">AzureRM.Insights</span></span>
* <span data-ttu-id="03e91-445">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-445">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-446">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-446">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="03e91-447">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="03e91-447">AzureRM.IotHub</span></span>
* <span data-ttu-id="03e91-448">IoTHub cmdlet에 인증서 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-448">Add Certificate support for IoTHub cmdlets</span></span>
* <span data-ttu-id="03e91-449">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-449">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-450">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-450">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="03e91-451">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="03e91-451">AzureRM.KeyVault</span></span>
* <span data-ttu-id="03e91-452">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-452">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-453">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-453">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-454">장기 실행 KeyVault cmdlet에 대한 -AsJob 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-454">Added -AsJob support for long-running KeyVault cmdlets.</span></span> <span data-ttu-id="03e91-455">선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-455">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
  * <span data-ttu-id="03e91-456">영향을 받는 cmdlet은 Remove-AzureRmKeyVault입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-456">Affected cmdlet is: Remove-AzureRmKeyVault</span></span>
* <span data-ttu-id="03e91-457">AAD 필터가 UPN 설정이 아닌 SPN을 제공된 UPN으로 설정하는 Set-AzureRmKeyVaultAccessPolicy에서 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-457">Fixed bug in Set-AzureRmKeyVaultAccessPolicy where the AAD filter was setting SPN to the provided UPN, rather than setting the UPN</span></span>
  - <span data-ttu-id="03e91-458">보다 자세한 내용은 다음 문제를 참조하세요. https://github.com/Azure/azure-powershell/issues/5201</span><span class="sxs-lookup"><span data-stu-id="03e91-458">See the following issue for more information: https://github.com/Azure/azure-powershell/issues/5201</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="03e91-459">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="03e91-459">AzureRM.LogicApp</span></span>
* <span data-ttu-id="03e91-460">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-460">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-461">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-461">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="03e91-462">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="03e91-462">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="03e91-463">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-463">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-464">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-464">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-465">Update-AzureRmMlCommitmentPlan에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-465">Obsoleted -Tags in favor of -Tag for Update-AzureRmMlCommitmentPlan</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="03e91-466">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="03e91-466">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="03e91-467">Remove-AzureRmMlOpCluster cmdlet에 IncludeAllResources 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-467">Add IncludeAllResources parameter to Remove-AzureRmMlOpCluster cmdlet</span></span>
  - <span data-ttu-id="03e91-468">이 스위치 매개 변수를 사용하면 원래 클러스터를 사용하여 만든 모든 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-468">Using this switch parameter will remove all resources that were created with the cluster originally</span></span>
* <span data-ttu-id="03e91-469">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-469">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-470">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-470">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="03e91-471">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="03e91-471">AzureRM.Media</span></span>
* <span data-ttu-id="03e91-472">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-472">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-473">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-473">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-474">Set-AzureRmMediaService 및 New-AzureRmMediaService에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-474">Obsoleted -Tags in favor of -Tag for Set-AzureRmMediaService and New-AzureRmMediaService</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="03e91-475">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="03e91-475">AzureRM.Network</span></span>
* <span data-ttu-id="03e91-476">장기 실행 Network cmdlet에 대한 -AsJob 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-476">Added -AsJob support for long-running Network cmdlets.</span></span> <span data-ttu-id="03e91-477">선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-477">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="03e91-478">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-478">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-479">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-479">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="03e91-480">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="03e91-480">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="03e91-481">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-481">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-482">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-482">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-483">New-AzureRmNotificationHubsNamespace 및 Set-AzureRmNotificationHubsNamespace에 -Tag를 사용하는 -Tags 사용하지를 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-483">Obsoleted -Tags in favor of -Tag for New-AzureRmNotificationHubsNamespace and Set-AzureRmNotificationHubsNamespace</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="03e91-484">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-484">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="03e91-485">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-485">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-486">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-486">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-487">New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace 및 Set-AzureRmOperationalInsightsWorkspace에 -Tag를 사용하는 -Tags 사용하지를 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-487">Obsoleted -Tags in favor of -Tag for New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace, and Set-AzureRmOperationalInsightsWorkspace</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="03e91-488">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="03e91-488">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="03e91-489">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-489">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-490">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-490">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="03e91-491">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03e91-491">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="03e91-492">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-492">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-493">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-493">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="03e91-494">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-494">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="03e91-495">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-495">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-496">Restore-AzureRmRecoveryServicesBackupItem cmdlet에 -UseOriginalStorageAccount 옵션을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-496">Added -UseOriginalStorageAccount option to the Restore-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>
  - <span data-ttu-id="03e91-497">이 플래그를 사용하면 사용자가 원래 VM과 최대한 가까운 복원된 VM의 구성이 유지하도록 원래 저장소 계정에 디스크를 복원하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-497">Enabling this flag results in restoring disks to their original storage accounts which allows users to maintain the configuration of restored VM as close to the original VMs as possible.</span></span>
  - <span data-ttu-id="03e91-498">복원 작업의 성능을 향상시키는 데에도 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-498">It also helps in improving the performance of the restore operation.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="03e91-499">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="03e91-499">AzureRM.RedisCache</span></span>
* <span data-ttu-id="03e91-500">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-500">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-501">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-501">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-502">방화벽 규칙에 대한 새로운 3개의 cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-502">Added  3 new cmdlets for firewall rules</span></span>
* <span data-ttu-id="03e91-503">지리적 복제에 대한 새로운 3개의 cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-503">Added  3 new cmdlets for geo replication</span></span>
* <span data-ttu-id="03e91-504">영역 및 태그에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-504">Added support for zones and tags</span></span>
* <span data-ttu-id="03e91-505">가능하면 ResourceGroup을 선택 사항으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-505">Make ResourceGroup as optional whenever possible.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="03e91-506">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="03e91-506">AzureRM.Relay</span></span>
* <span data-ttu-id="03e91-507">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-507">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-508">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-508">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="03e91-509">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="03e91-509">AzureRM.Resources</span></span>
* <span data-ttu-id="03e91-510">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-510">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-511">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-511">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-512">장기 실행 Resources cmdlet에 대한 -AsJob 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-512">Added -AsJob support for long-running Resources cmdlets.</span></span> <span data-ttu-id="03e91-513">선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-513">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="03e91-514">명명 규칙을 준수하도록 Get-AzureRmProviderOperation에서 Get-AzureRmResourceProviderAction에 별칭을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-514">Added alias from Get-AzureRmProviderOperation to Get-AzureRmResourceProviderAction to conform with naming conventions</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="03e91-515">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="03e91-515">AzureRM.Scheduler</span></span>
* <span data-ttu-id="03e91-516">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-516">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-517">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-517">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservermanagement"></a><span data-ttu-id="03e91-518">AzureRM.ServerManagement</span><span class="sxs-lookup"><span data-stu-id="03e91-518">AzureRM.ServerManagement</span></span>
* <span data-ttu-id="03e91-519">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-519">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-520">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-520">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-521">New-AzureRmServerManagementNode 및 New-AzureRmServerManagementGateway에 -Tag를 사용하는 -Tags를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-521">Obsoleted -Tags in favor of -Tag for New-AzureRmServerManagementNode and New-AzureRmServerManagementGateway</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="03e91-522">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="03e91-522">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="03e91-523">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-523">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-524">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-524">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="03e91-525">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="03e91-525">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="03e91-526">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-526">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-527">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-527">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsiterecovery"></a><span data-ttu-id="03e91-528">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-528">AzureRM.SiteRecovery</span></span>
* <span data-ttu-id="03e91-529">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-529">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-530">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-530">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="03e91-531">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="03e91-531">AzureRM.Sql</span></span>
* <span data-ttu-id="03e91-532">감사 명령 매개 변수 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-532">Update the Auditing commands parameters description</span></span>
* <span data-ttu-id="03e91-533">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-533">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-534">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-534">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-535">장기 실행 cmdlet에 -AsJob 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-535">Added -AsJob parameter to long running cmdlets</span></span>
* <span data-ttu-id="03e91-536">Get-AzureRmSqlServiceObjective에서 -DatabaseName 매개 변수를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-536">Obsoleted -DatabaseName parameter from Get-AzureRmSqlServiceObjective</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="03e91-537">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-537">AzureRM.Storage</span></span>
* <span data-ttu-id="03e91-538">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-538">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-539">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-539">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-540">-EnableEncryptionService None 매개 변수를 사용하여 New-AzureRMStorageAccount 실행 cmdlet의 null 참조 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-540">Fix a null reference issue of run cmdlet New-AzureRMStorageAccount with parameter -EnableEncryptionService None</span></span>
* <span data-ttu-id="03e91-541">장기 실행 Storage cmdlet에 대한 -AsJob 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-541">Added -AsJob support for long-running Storage cmdlets.</span></span> <span data-ttu-id="03e91-542">선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-542">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="03e91-543">영향을 받는 cmdlet은 저장소 계정 및 네트워크 규칙에 대한 New-, Remove-, Add- 및 Update-입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-543">Affected cmdlets are New-, Remove-, Add-, and Update- for Storage Account and Storage Account Network Rule.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="03e91-544">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="03e91-544">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="03e91-545">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-545">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-546">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-546">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="03e91-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="03e91-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="03e91-548">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-548">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-549">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-549">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="03e91-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="03e91-550">AzureRM.Websites</span></span>
* <span data-ttu-id="03e91-551">유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-551">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="03e91-552">현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-552">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="03e91-553">장기 실행 Websites cmdlet에 대한 -AsJob 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-553">Added -AsJob support for long-running Websites cmdlets.</span></span> <span data-ttu-id="03e91-554">선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-554">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
     - <span data-ttu-id="03e91-555">영향을 받는 cmdlet은 WebApps, AppServicePlan 및 Slots에 대한 New-, Remove-, Add- 및 Set-입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-555">Affected cmdlets are New-, Remove-, Add-, and Set- for WebApps, AppServicePlan and Slots</span></span>

## <a name="2017128-version-511"></a><span data-ttu-id="03e91-556">2017.12.8 버전 5.1.1</span><span class="sxs-lookup"><span data-stu-id="03e91-556">2017.12.8 Version 5.1.1</span></span>
* <span data-ttu-id="03e91-557">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="03e91-557">AnalysisServices</span></span>
  - <span data-ttu-id="03e91-558">모든 클라우드가 지원되도록 위치 확인 집합을 동적 조회로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-558">Change validate set of location to dynamic lookup so that all clouds are supported.</span></span>
* <span data-ttu-id="03e91-559">Automation</span><span class="sxs-lookup"><span data-stu-id="03e91-559">Automation</span></span>
  - <span data-ttu-id="03e91-560">Import-AzureRMAutomationRunbook으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-560">Update to Import-AzureRMAutomationRunbook</span></span>
    - <span data-ttu-id="03e91-561">이제 Python2 Runbook에 대한 지원이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-561">Support is now being provided for Python2 runbooks</span></span>
* <span data-ttu-id="03e91-562">Batch</span><span class="sxs-lookup"><span data-stu-id="03e91-562">Batch</span></span>
  - <span data-ttu-id="03e91-563">리소스 그룹이 없는 계정 작업으로 리소스 그룹을 자동 검색하지 못하는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-563">Fixed a bug where account operations without a resource group failed to auto-detect the resource group</span></span>
* <span data-ttu-id="03e91-564">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="03e91-564">Compute</span></span>
  - <span data-ttu-id="03e91-565">Get-AzureRmComputeResourceSku가 영역 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-565">Get-AzureRmComputeResourceSku shows zone information.</span></span>
  - <span data-ttu-id="03e91-566">문제 https://github.com/Azure/azure-powershell/issues/5038의 수정을 위해 Disable-AzureRmVmssDiskEncryption 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-566">Update Disable-AzureRmVmssDiskEncryption to fix issue https://github.com/Azure/azure-powershell/issues/5038</span></span>
  - <span data-ttu-id="03e91-567">장기 실행 Compute cmdlet에 대한 -AsJob 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-567">Added -AsJob support for long-running Compute cmdlets.</span></span> <span data-ttu-id="03e91-568">선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-568">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="03e91-569">영향을 받는 cmdlet은 Virtual Machines 및 Virtual Machine Scale Sets에 대한 New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-569">Affected cmdlets include: New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlets for Virtual Machines and Virtual Machine Scale Sets</span></span>
    - <span data-ttu-id="03e91-570">단순한 매개 변수 집합이 New-AzureRmVM에 추가되었습니다. 따라서 스마트 기본값을 사용하여 Virtual Machine과 필요한 모든 리소스가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-570">Added simplified parameter set to New-AzureRmVM, which creates a Virtual Machine and all required resources using smart defaults</span></span>
* <span data-ttu-id="03e91-571">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="03e91-571">ContainerInstance</span></span>
  - <span data-ttu-id="03e91-572">Azure Container Instance SDK 2017-10-01 적용</span><span class="sxs-lookup"><span data-stu-id="03e91-572">Apply Azure Container Instance SDK 2017-10-01</span></span>
    - <span data-ttu-id="03e91-573">컨테이너 실행 완료 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-573">Support container run-to-completion</span></span>
    - <span data-ttu-id="03e91-574">Azure 파일 볼륨 탑재 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-574">Support Azure File volume mount</span></span>
    - <span data-ttu-id="03e91-575">공용 IP에 대한 여러 포트 열기 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-575">Support opening multiple ports for public IP</span></span>
* <span data-ttu-id="03e91-576">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="03e91-576">ContainerRegistry</span></span>
  - <span data-ttu-id="03e91-577">지역에서 복제 및 웹후크에 대한 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="03e91-577">New cmdlets for geo-replication and webhooks</span></span>
    - <span data-ttu-id="03e91-578">Get/New/Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="03e91-578">Get/New/Remove-AzureRmContainerRegistryReplication</span></span>
    - <span data-ttu-id="03e91-579">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="03e91-579">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span></span>
* <span data-ttu-id="03e91-580">DataFactories</span><span class="sxs-lookup"><span data-stu-id="03e91-580">DataFactories</span></span>
    - <span data-ttu-id="03e91-581">이제 자격 증명 암호화 기능은 "원격 액세스"가 사용된 경우(네트워크 사용) 및 "원격 액세스"가 사용되지 않는 경우(로컬 컴퓨터) 모두에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-581">Credential encryption functionality now works with both "Remote Access" enabled (Over Network) and "Remote Access" disabled (Local Machine).</span></span>
* <span data-ttu-id="03e91-582">DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="03e91-582">DataFactoryV2</span></span>
  - <span data-ttu-id="03e91-583">두 개의 새로운 cmdlet 추가: Update-AzureRmDataFactoryV2 및 Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="03e91-583">Added two new cmdlets: Update-AzureRmDataFactoryV2 and Stop-AzureRmDataFactoryV2PipelineRun</span></span>
* <span data-ttu-id="03e91-584">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="03e91-584">DataLakeAnalytics</span></span>
  - <span data-ttu-id="03e91-585">Submit-AzureRmDataLakeAnalyticsJob에 ScriptParameter라는 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-585">Added a parameter called ScriptParameter to Submit-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="03e91-586">ScriptParameter에 대한 자세한 정보는 Submit-AzureRmDataLakeAnalyticsJob에서 Get-Help를 사용하여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-586">Detailed information about ScriptParameter can be found using Get-Help on Submit-AzureRmDataLakeAnalyticsJob</span></span>
  - <span data-ttu-id="03e91-587">New-AzureRmDataLakeAnalyticsAccount의 경우 MaxDegreeOfParallelism 매개 변수가 MaxAnalyticsUnits로 변경됨</span><span class="sxs-lookup"><span data-stu-id="03e91-587">For New-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="03e91-588">MaxAnalyticsUnits: MaxDegreeOfParallelism 매개 변수에 대한 별칭이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-588">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="03e91-589">New-AzureRmDataLakeAnalyticsComputePolicy의 경우 MaxDegreeOfParallelismPerJob 매개 변수가 MaxAnalyticsUnitsPerJob으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="03e91-589">For New-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="03e91-590">MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob 매개 변수에 대한 별칭이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-590">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
  - <span data-ttu-id="03e91-591">Set-AzureRmDataLakeAnalyticsAccount의 경우 MaxDegreeOfParallelism 매개 변수가 MaxAnalyticsUnits로 변경됨</span><span class="sxs-lookup"><span data-stu-id="03e91-591">For Set-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="03e91-592">MaxAnalyticsUnits: MaxDegreeOfParallelism 매개 변수에 대한 별칭이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-592">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="03e91-593">Submit-AzureRmDataLakeAnalyticsJob의 경우 DegreeOfParallelism 매개 변수가 AnalyticsUnits로 변경됨</span><span class="sxs-lookup"><span data-stu-id="03e91-593">For Submit-AzureRmDataLakeAnalyticsJob, changed the parameter DegreeOfParallelism to AnalyticsUnits</span></span>
    - <span data-ttu-id="03e91-594">AnalyticsUnits: DegreeOfParallelism 매개 변수에 대한 별칭이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-594">Added an alias for the parameter AnalyticsUnits: DegreeOfParallelism</span></span>
  - <span data-ttu-id="03e91-595">Update-AzureRmDataLakeAnalyticsComputePolicy의 경우 MaxDegreeOfParallelismPerJob 매개 변수가 MaxAnalyticsUnitsPerJob으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="03e91-595">For Update-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="03e91-596">MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob 매개 변수에 대한 별칭이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-596">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
* <span data-ttu-id="03e91-597">MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="03e91-597">MachineLearningCompute</span></span>
  - <span data-ttu-id="03e91-598">Set-AzureRmMlOpCluster 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-598">Add Set-AzureRmMlOpCluster</span></span>
    - <span data-ttu-id="03e91-599">클러스터의 에이전트 개수 또는 SSL 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-599">Update a cluster's agent count or SSL configuration</span></span>
  - <span data-ttu-id="03e91-600">오케스트레이터 속성은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-600">Orchestrator properties are optional</span></span>
    - <span data-ttu-id="03e91-601">서비스에서 서비스 주체를 생성하므로(제공되지 않은 경우) 오케스트레이터 속성은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-601">The service will create a service principal if not provided, so the orchestrator properties are now optional</span></span>
* <span data-ttu-id="03e91-602">PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="03e91-602">PowerBIEmbedded</span></span>
  - <span data-ttu-id="03e91-603">Power BI Embedded Capacity cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-603">Add support for Power BI Embedded Capacity cmdlets</span></span>
  - <span data-ttu-id="03e91-604">새 Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity에 대한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-604">New Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Gets the details of a PowerBI Embedded Capacity.</span></span>
  - <span data-ttu-id="03e91-605">새 Cmdlet New-AzureRmPowerBIEmbeddedCapacity - 새 PowerBI Embedded Capacity를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-605">New Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Creates a new PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="03e91-606">새 Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-606">New Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Deletes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="03e91-607">새 Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-607">New Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Resumes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="03e91-608">새 Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-608">New Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Suspends an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="03e91-609">새 Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity 인스턴스의 존재 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-609">New Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Tests the existence of an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="03e91-610">새 Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-610">New Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Modifies an instance of PowerBI Embedded Capacity</span></span>
* <span data-ttu-id="03e91-611">프로필</span><span class="sxs-lookup"><span data-stu-id="03e91-611">Profile</span></span>
  - <span data-ttu-id="03e91-612">USGovernmentActiveDirectoryEndpoint가 https://login.microsoftonline.us/로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="03e91-612">Updated USGovernmentActiveDirectoryEndpoint to https://login.microsoftonline.us/</span></span>
    - <span data-ttu-id="03e91-613">Azure Government 끝점 매핑에 대한 보다 자세한 내용은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span><span class="sxs-lookup"><span data-stu-id="03e91-613">For more information about the Azure Government endpoint mappings, please see the following: https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span></span>
    - <span data-ttu-id="03e91-614">cmdlet에 대한 -AsJob 지원이 추가됨. 선택된 cmdlet을 사용하여 백그라운드에서 실행하고 작업을 반환하여 진행률 추적 및 제어</span><span class="sxs-lookup"><span data-stu-id="03e91-614">Added -AsJob support for cmdlets, enabling selected cmdlets to execute in the background and return a job to track and control progress</span></span>
    - <span data-ttu-id="03e91-615">-AsJob 매개 변수가 Get-AzureRmSubscription cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-615">Added -AsJob parameter to Get-AzureRmSubscription cmdlet</span></span>
* <span data-ttu-id="03e91-616">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-616">RecoveryServices.Backup</span></span>
  - <span data-ttu-id="03e91-617">버그 수정됨 - Get-AzureRmRecoveryServicesBackupItem은 컨테이너 이름 필터에 대해 대/소문자를 구분하지 않는 비교를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-617">Fixed bug - Get-AzureRmRecoveryServicesBackupItem should do case insensitive comparison for container name filter.</span></span>
  - <span data-ttu-id="03e91-618">버그 수정됨 - AzureVmItem에는 백업 작업이 마지막으로 발생한 시간(LastBackupTime)을 보여 주는 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-618">Fixed bug - AzureVmItem now has a property that shows the last time a backup operation has happened - LastBackupTime.</span></span>
* <span data-ttu-id="03e91-619">리소스</span><span class="sxs-lookup"><span data-stu-id="03e91-619">Resources</span></span>
  - <span data-ttu-id="03e91-620">Get-AzureRMRoleAssignment가 사용자 지정 역할에 대한 roledefiniton 이름 없이 할당하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-620">Fixed issue where Get-AzureRMRoleAssignment would result in a assignments without roledefiniton name for custom roles</span></span>
    - <span data-ttu-id="03e91-621">이제 사용자는 역할 유형에 관계없이 roledefinition이 있는 할당으로 Get-AzureRMRoleAssignment를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-621">Users can now use Get-AzureRMRoleAssignment with assignments having roledefinition names irrespective of the type of role</span></span>
  - <span data-ttu-id="03e91-622">assignablescopes에 새 범위가 있을 때 RD를 throw하는 데 사용된 Set-AzureRMRoleRoleDefinition이 오류를 찾을 수 없는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-622">Fixed issue where Set-AzureRMRoleRoleDefinition used to throw RD not found error when there was a new scope in assignablescopes</span></span>
    - <span data-ttu-id="03e91-623">이제 사용자는 범위의 위치와 관계없이 새 범위를 포함하여 할당 가능한 범위로 Set-AzureRMRoleRoleDefinition을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-623">Users can now use Set-AzureRMRoleRoleDefinition with assignable scopes including new scopes irrespective of the position of the scope</span></span>
  - <span data-ttu-id="03e91-624">범위를 "/"로 끝내도록 허용</span><span class="sxs-lookup"><span data-stu-id="03e91-624">Allow scopes to end with "/"</span></span>
    - <span data-ttu-id="03e91-625">사용자는 이제 API 및 CLI와 일치하고 범위가 "/"로 끝나는 RoleDefinition 및 RoleAssignment commandlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-625">Users can now use RoleDefinition and RoleAssignment commandlets with scopes ending with "/" ,consistent with API and CLI</span></span>
  - <span data-ttu-id="03e91-626">사용자가 위임 플래그를 사용하여 RoleAssignment를 만들도록 허용</span><span class="sxs-lookup"><span data-stu-id="03e91-626">Allow users to create RoleAssignment using delegation flag</span></span>
    - <span data-ttu-id="03e91-627">사용자는 위임 플래그를 추가하는 옵션과 함께 New-AzureRMRoleAssignment를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-627">Users can now use New-AzureRMRoleAssignment with an option of adding the delegation flag</span></span>
  - <span data-ttu-id="03e91-628">RoleAssignment가 범위 매개 변수를 따르도록 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-628">Fix RoleAssignment get to respect the scope parameter</span></span>
  - <span data-ttu-id="03e91-629">New-AzureRmRoleAssignment Commandlet에서 ServicePrincipalName에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-629">Add an alias for ServicePrincipalName in the New-AzureRmRoleAssignment Commandlet</span></span>
    - <span data-ttu-id="03e91-630">사용자가 New-AzureRmRoleAssignment Commandlet을 사용할 때 ServicePrincipalName 대신 ApplicationId를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-630">Users can now use the ApplicationId instead of the ServicePrincipalName when using the New-AzureRmRoleAssignment commandlet</span></span>
* <span data-ttu-id="03e91-631">SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-631">SiteRecovery</span></span>
  - <span data-ttu-id="03e91-632">향후 주요 변경 릴리스에 대한 준비에서, 이 모듈의 모든 cmdlet에 대한 사용 중단 경고를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-632">Add deprecation warnings for all cmdlets in this module in preparation for the next breaking change release.</span></span>
    - <span data-ttu-id="03e91-633">AzureRM에서 cmdlet을 마이그레이션하는 방법에 대한 자세한 내용은 다음 주요 변경 사항 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-633">Please see the upcoming breaking changes guide for more information on how to migrate your cmdlets from AzureRM.</span></span>
* <span data-ttu-id="03e91-634">Sql</span><span class="sxs-lookup"><span data-stu-id="03e91-634">Sql</span></span>
  - <span data-ttu-id="03e91-635">Set-AzureRmSqlDatabase를 사용하여 데이터베이스 이름을 바꾸는 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-635">Added ability to rename database using Set-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="03e91-636">문제 https://github.com/Azure/azure-powershell/issues/4974 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-636">Fixed issue https://github.com/Azure/azure-powershell/issues/4974</span></span>
    - <span data-ttu-id="03e91-637">감사 cmdlet에 대해 유효하지 않은 AUDIT_CHANGED_GROUP 값을 제공하면 더 이상 오류가 발생하지 않으며 향후 릴리스에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-637">Providing invalid AUDIT_CHANGED_GROUP value for auditing cmdlets no longer throws an error and will be removed in an upcoming release.</span></span>
  - <span data-ttu-id="03e91-638">문제 https://github.com/Azure/azure-powershell/issues/5046 해결</span><span class="sxs-lookup"><span data-stu-id="03e91-638">Fixed issue https://github.com/Azure/azure-powershell/issues/5046</span></span>
    - <span data-ttu-id="03e91-639">감사 cmdlet의 AuditAction 매개 변수가 더 이상 무시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-639">AuditAction parameter in auditing cmdlets is no longer being ignored</span></span>
  - <span data-ttu-id="03e91-640">'보조' StorageKeyType이 제공된 경우 감사 cmdlet에서 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-640">Fixed an issue in Auditing cmdlets when 'Secondary' StorageKeyType is provided</span></span>
    - <span data-ttu-id="03e91-641">Blob 감사를 설정할 때, StorageKeyType 매개 변수에 '보조' 값을 제공할 때 보조 키 대신, 주 저장소 계정 키가 사용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-641">When setting blob auditing, the primary storage account key was used instead of the secondary key when providing 'Secondary' value for StorageKeyType parameter.</span></span>
  - <span data-ttu-id="03e91-642">Set-AzureRmSqlServerTransparentDataEncryptionProtector에서 확인 메시지의 문구 변경</span><span class="sxs-lookup"><span data-stu-id="03e91-642">Changing the wording for confirmation message from Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>
* <span data-ttu-id="03e91-643">Azure(RDFE)</span><span class="sxs-lookup"><span data-stu-id="03e91-643">Azure (RDFE)</span></span>
    - <span data-ttu-id="03e91-644">모든 RemoteApp Cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="03e91-644">Removed all RemoteApp Cmdles</span></span>
* <span data-ttu-id="03e91-645">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-645">Azure.Storage</span></span>
    - <span data-ttu-id="03e91-646">Azure Storage 클라이언트 라이브러리 8.6.0 및 Azure Storage DataMovement 라이브러리 0.6.5로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="03e91-646">Upgrade to Azure Storage Client Library 8.6.0 and Azure Storage DataMovement Library 0.6.5</span></span>

## <a name="20171110-version-501"></a><span data-ttu-id="03e91-647">2017.11.10 버전 5.0.1</span><span class="sxs-lookup"><span data-stu-id="03e91-647">2017.11.10 Version 5.0.1</span></span>
* <span data-ttu-id="03e91-648">다음과 같은 모듈에서 실행할 때 몇 가지 cmdlet이 실패하는 어셈블리 로딩 문제 해결:</span><span class="sxs-lookup"><span data-stu-id="03e91-648">Fixed assembly loading issue that caused some cmdlets to fail when executing in the following modules:</span></span>
  - <span data-ttu-id="03e91-649">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="03e91-649">AzureRM.ApiManagement</span></span>
  - <span data-ttu-id="03e91-650">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-650">AzureRM.Backup</span></span>
  - <span data-ttu-id="03e91-651">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-651">AzureRM.Batch</span></span>
  - <span data-ttu-id="03e91-652">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="03e91-652">AzureRM.Compute</span></span>
  - <span data-ttu-id="03e91-653">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="03e91-653">AzureRM.DataFactories</span></span>
  - <span data-ttu-id="03e91-654">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="03e91-654">AzureRM.HDInsight</span></span>
  - <span data-ttu-id="03e91-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="03e91-655">AzureRM.KeyVault</span></span>
  - <span data-ttu-id="03e91-656">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03e91-656">AzureRM.RecoveryServices</span></span>
  - <span data-ttu-id="03e91-657">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-657">AzureRM.RecoveryServices.Backup</span></span>
  - <span data-ttu-id="03e91-658">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-658">AzureRM.RecoveryServices.SiteRecovery</span></span>
  - <span data-ttu-id="03e91-659">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="03e91-659">AzureRM.RedisCache</span></span>
  - <span data-ttu-id="03e91-660">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-660">AzureRM.SiteRecovery</span></span>
  - <span data-ttu-id="03e91-661">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="03e91-661">AzureRM.Sql</span></span>
  - <span data-ttu-id="03e91-662">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-662">AzureRM.Storage</span></span>
  - <span data-ttu-id="03e91-663">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="03e91-663">AzureRM.StreamAnalytics</span></span>

## <a name="2017118---version-500"></a><span data-ttu-id="03e91-664">2017.11.8 - 버전 5.0.0</span><span class="sxs-lookup"><span data-stu-id="03e91-664">2017.11.8 - Version 5.0.0</span></span>
* <span data-ttu-id="03e91-665">참고: 이는 중요 변경 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-665">NOTE: This is a breaking change release.</span></span> <span data-ttu-id="03e91-666">중요 변경 사항의 전체 목록은 마이그레이션 가이드(https://aka.ms/azps-migration-guide))를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-666">Please see the migration guide (https://aka.ms/azps-migration-guide) for a full list of introduced breaking changes.</span></span>
* <span data-ttu-id="03e91-667">AzureRM의 모든 cmdlet는 이제 온라인 도움말을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-667">All cmdlets in AzureRM now support online help</span></span>
  - <span data-ttu-id="03e91-668">-Online 매개 변수와 함께 Get-Help를 실행하여 기본 인터넷 브라우저에서 온라인 도움말을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-668">Run Get-Help with the -Online parameter to open the online help in your default Internet browser</span></span>
* <span data-ttu-id="03e91-669">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="03e91-669">AnalysisServices</span></span>
  * <span data-ttu-id="03e91-670">동기화를 위해 새로운 AsAzure REST API로 작동하도록 Synchronize-AzureAsInstance 명령 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-670">Fixed Synchronize-AzureAsInstance command to work with new AsAzure REST API for sync</span></span>
* <span data-ttu-id="03e91-671">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="03e91-671">ApiManagement</span></span>
  * <span data-ttu-id="03e91-672">이 릴리스의 ApiManagement에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-672">Please see the migration guide for breaking changes made to ApiManagement this release</span></span>
  * <span data-ttu-id="03e91-673">문제 https://github.com/Azure/azure-powershell/issues/4510의 수정을 위해 Cmdlet Get-AzureRmApiManagementUser 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-673">Updated Cmdlet Get-AzureRmApiManagementUser to fix issue https://github.com/Azure/azure-powershell/issues/4510</span></span>
  * <span data-ttu-id="03e91-674">https://github.com/Azure/azure-powershell/issues/4069의 경로가 비어 있는 API 생성을 위해 Cmdlet New-AzureRmApiManagementApi 업데이트</span><span class="sxs-lookup"><span data-stu-id="03e91-674">Updated Cmdlet New-AzureRmApiManagementApi to create Api with Empty Path https://github.com/Azure/azure-powershell/issues/4069</span></span>
* <span data-ttu-id="03e91-675">ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-675">ApplicationInsights</span></span>
  * <span data-ttu-id="03e91-676">applicaiton insights 리소스를 가져오기/만들기/제거하기 위해 명령 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-676">Add commands to get/create/remove applicaiton insights resource</span></span>
    - <span data-ttu-id="03e91-677">Get AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-677">Get-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="03e91-678">Get AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-678">New-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="03e91-679">Get AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="03e91-679">Remove-AzureRmApplicationInsights</span></span>
  * <span data-ttu-id="03e91-680">application insights 리소스의 가격 책정/일일 상한선을 가져오기/업데이트하기 위해 명령 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-680">Add commands to get/update pricing/daily cap of applicaiton insights resource</span></span>
    - <span data-ttu-id="03e91-681">Get-AzureRmApplicationInsights -IncludeDailyCap</span><span class="sxs-lookup"><span data-stu-id="03e91-681">Get-AzureRmApplicationInsights -IncludeDailyCap</span></span>
    - <span data-ttu-id="03e91-682">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="03e91-682">Set-AzureRmApplicationInsightsPricingPlan</span></span>
    - <span data-ttu-id="03e91-683">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="03e91-683">Set-AzureRmApplicationInsightsDailyCap</span></span>
  * <span data-ttu-id="03e91-684">applicaiton insights 리소스의 연속 내보내기를 가져오기/만들기/업데이트하기/제거하기 위해 명령 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-684">Add commands to get/create/update/remove continuous export of applicaiton insights resource</span></span>
    - <span data-ttu-id="03e91-685">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="03e91-685">Get-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="03e91-686">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="03e91-686">Set-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="03e91-687">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="03e91-687">New-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="03e91-688">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="03e91-688">Remove-AzureRmApplicationInsightsContinuousExport</span></span>
  * <span data-ttu-id="03e91-689">applicaiton insights 리소스의 api 키를 가져오기/만들기/제거하기 위해 명령 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-689">Add commands to get/create/remove api keys of applicaiton insights resoruce</span></span>
    - <span data-ttu-id="03e91-690">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="03e91-690">Get-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="03e91-691">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="03e91-691">New-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="03e91-692">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="03e91-692">Remove-AzureRmApplicationInsightsApiKey</span></span>
* <span data-ttu-id="03e91-693">AzureBatch</span><span class="sxs-lookup"><span data-stu-id="03e91-693">AzureBatch</span></span>
  * <span data-ttu-id="03e91-694">`New-AzureRmBatchAccount`에 새 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-694">Added new parameters to `New-AzureRmBatchAccount`.</span></span>
    - <span data-ttu-id="03e91-695">`PoolAllocationMode`: 배치 계정에서 풀을 만드는 데 사용하는 할당 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-695">`PoolAllocationMode`: The allocation mode to use for creating pools in the Batch account.</span></span> <span data-ttu-id="03e91-696">사용자의 구독에서 풀 노드를 할당하는 배치 계정을 만들려면 이를 `UserSubscription`으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-696">To create a Batch account which allocates pool nodes in the user's subscription, set this to `UserSubscription`.</span></span>
    - <span data-ttu-id="03e91-697">`KeyVaultId`: 배치 계정과 연결된 Azure Key Vault의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-697">`KeyVaultId`: The resource ID of the Azure key vault associated with the Batch account.</span></span>
    - <span data-ttu-id="03e91-698">`KeyVaultUrl`: 배치 계정과 연결된 Azure Key Vault의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-698">`KeyVaultUrl`: The URL of the Azure key vault associated with the Batch account.</span></span>
  * <span data-ttu-id="03e91-699">매개 변수를 `New-AzureBatchTask`로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-699">Updated parameters to `New-AzureBatchTask`.</span></span>
    - <span data-ttu-id="03e91-700">`RunElevated` 스위치를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-700">Removed the `RunElevated` switch.</span></span> <span data-ttu-id="03e91-701">`UserIdentity` 매개 변수가 `RunElevated`를 대체하기 위해 추가되었으며, 아래와 같이 `PSUserIdentity`를 구성하여 동등한 동작을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-701">The `UserIdentity` parameter has been added to replace `RunElevated`, and the equivalent behavior can be achieved by constructing a `PSUserIdentity` as shown below:</span></span>
      - <span data-ttu-id="03e91-702">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span><span class="sxs-lookup"><span data-stu-id="03e91-702">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span></span>
      - <span data-ttu-id="03e91-703">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span><span class="sxs-lookup"><span data-stu-id="03e91-703">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span></span>
    - <span data-ttu-id="03e91-704">`AuthenticationTokenSettings` 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-704">Added the `AuthenticationTokenSettings` parameter.</span></span> <span data-ttu-id="03e91-705">이 매개 변수를 사용하면 실행할 때 일괄 처리 서비스가 인증 토큰을 작업에 제공하도록 요청할 수 있어, 일괄 처리 서비스에 요청을 발행하기 위해 배치 계정 키를 작업에 전달할 필요가 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-705">This parameter allows you to request the Batch service provide an authentication token to the task when it runs, avoiding the need to pass Batch account keys to the task in order to issue requests to the Batch service.</span></span>
    - <span data-ttu-id="03e91-706">`ContainerSettings` 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-706">Added the `ContainerSettings` parameter.</span></span>
      - <span data-ttu-id="03e91-707">이 매개 변수를 사용하면 일괄 처리 서비스가 컨테이너 내의 작업을 실행하도록 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-707">This parameter allows you to request the Batch service run the task inside a container.</span></span>
    - <span data-ttu-id="03e91-708">`OutputFiles` 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-708">Added the `OutputFiles` parameter.</span></span>
      - <span data-ttu-id="03e91-709">이 매개 변수를 사용하면 완료된 후 Azure Storage에 파일을 업로드하는 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-709">This parameter allows you to configure the task to upload files to Azure Storage after it has finished.</span></span>
  * <span data-ttu-id="03e91-710">매개 변수를 `New-AzureBatchPool`로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-710">Updated parameters to `New-AzureBatchPool`.</span></span>
    - <span data-ttu-id="03e91-711">`UserAccounts` 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-711">Added the `UserAccounts` parameter.</span></span>
      - <span data-ttu-id="03e91-712">이 매개 변수는 풀의 각 노드에서 만든 사용자 계정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-712">This parameter defines user accounts created on each node in the pool.</span></span>
    - <span data-ttu-id="03e91-713">`TargetLowPriorityComputeNodes`를 추가하고 `TargetDedicated`의 이름을 `TargetDedicatedComputeNodes`으로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-713">Added `TargetLowPriorityComputeNodes` and renamed `TargetDedicated` to `TargetDedicatedComputeNodes`.</span></span>
      - <span data-ttu-id="03e91-714">`TargetDedicatedComputeNodes` 매개 변수에 대해 `TargetDedicated` 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-714">A `TargetDedicated` alias was created for the `TargetDedicatedComputeNodes` parameter.</span></span>
    - <span data-ttu-id="03e91-715">`NetworkConfiguration` 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-715">Added the `NetworkConfiguration` parameter.</span></span>
      - <span data-ttu-id="03e91-716">이 매개 변수를 사용하면 풀 네트워크 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-716">This parameter allows you to configure the pools network settings.</span></span>
  * <span data-ttu-id="03e91-717">매개 변수를 `New-AzureBatchCertificate`로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-717">Updated parameters to `New-AzureBatchCertificate`.</span></span>
    - <span data-ttu-id="03e91-718">`Password` 매개 변수가 이제 `SecureString`이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-718">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="03e91-719">매개 변수를 `New-AzureBatchComputeNodeUser`로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-719">Updated parameters to `New-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="03e91-720">`Password` 매개 변수가 이제 `SecureString`이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-720">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="03e91-721">매개 변수를 `Set-AzureBatchComputeNodeUser`로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-721">Updated parameters to `Set-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="03e91-722">`Password` 매개 변수가 이제 `SecureString`이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-722">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="03e91-723">`Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, 및 `Remove-AzureBatchNodeFile`에서 `Name` 매개 변수의 이름이 `Path`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-723">Renamed the `Name` parameter to `Path` on `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, and `Remove-AzureBatchNodeFile`.</span></span>
    - <span data-ttu-id="03e91-724">`Path` 매개 변수에 대해 `Name` 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-724">A `Name` alias was created for the `Path` parameter.</span></span>
  * <span data-ttu-id="03e91-725">개체에 대한 변경 사항</span><span class="sxs-lookup"><span data-stu-id="03e91-725">Changes to objects</span></span>
    - <span data-ttu-id="03e91-726">전체 목록은 일괄 처리 변경 로그를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-726">Please see the Batch change log for the full list</span></span>
  * <span data-ttu-id="03e91-727">Azure Active Directory 기반 인증에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-727">Added support for Azure Active Directory based authentication.</span></span>
    - <span data-ttu-id="03e91-728">Azure Active Directory 인증을 사용하려면 `Get-AzureRmBatchAccount` cmdlet를 사용하여 `BatchAccountContext` 개체를 검색하고 이 `BatchAccountContext`를 일괄 처리 서비스 cmdlet의 `-BatchContext` 매개 변수에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-728">To use Azure Active Directory authentication, retrieve a `BatchAccountContext` object using the `Get-AzureRmBatchAccount` cmdlet, and supply this `BatchAccountContext` to the `-BatchContext` parameter of a Batch service cmdlet.</span></span> <span data-ttu-id="03e91-729">Azure Active Directory 인증은 `PoolAllocationMode = UserSubscription`이 있는 계정에 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-729">Azure Active Directory authentication is mandatory for accounts with `PoolAllocationMode = UserSubscription`.</span></span>
    - <span data-ttu-id="03e91-730">기존 계정 또는 `PoolAllocationMode = BatchService`로 만든 새 계정의 경우, `Get-AzureRmBatchAccoutKeys` cmdlet를 사용하는 `BatchAccountContext` 개체를 검색하여 공유 키 인증을 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-730">For existing accounts or for new accounts created with `PoolAllocationMode = BatchService`, you may continue to use shared key authentication by retrieving a `BatchAccountContext` object using the `Get-AzureRmBatchAccoutKeys` cmdlet.</span></span>
* <span data-ttu-id="03e91-731">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="03e91-731">Compute</span></span>
  * <span data-ttu-id="03e91-732">Azure Disk Encryption 확장 명령</span><span class="sxs-lookup"><span data-stu-id="03e91-732">Azure Disk Encryption Extension Commands</span></span>
    - <span data-ttu-id="03e91-733">'Set-AzureRmVmDiskEncryptionExtension'에 대한 새 매개 변수': '-EncryptFormatAll' 암호화 형식 데이터 디스크</span><span class="sxs-lookup"><span data-stu-id="03e91-733">New Parameter for 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' encrypt formats data disks</span></span>
    - <span data-ttu-id="03e91-734">'Set-AzureRmVmDiskEncryptionExtension'에 대한 새로운 매개 변수: '-ExtensionPublisherName' 및 '-ExtensionType'이 다른 확장 버전으로 전환 허용</span><span class="sxs-lookup"><span data-stu-id="03e91-734">New Parameters for 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="03e91-735">'Disable-AzureRmVmDiskEncryption'에 대한 새로운 매개 변수: '-ExtensionPublisherName' 및 '-ExtensionType'이 다른 확장 버전으로 전환 허용</span><span class="sxs-lookup"><span data-stu-id="03e91-735">New Parameters for 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="03e91-736">'Get-AzureRmVmDiskEncryptionStatus'에 대한 새로운 매개 변수: '-ExtensionPublisherName' 및 '-ExtensionType'이 다른 확장 버전으로 전환 허용</span><span class="sxs-lookup"><span data-stu-id="03e91-736">New Parameters for 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
* <span data-ttu-id="03e91-737">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="03e91-737">DataLakeAnalytics</span></span>
  * <span data-ttu-id="03e91-738">이 릴리스의 DataLakeAnalytics에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-738">Please see the migration guide for breaking changes made to DataLakeAnalytics this release</span></span>
  * <span data-ttu-id="03e91-739">Get-AzureRmDataLakeAnalyticsAccount의 두 가지 OutputTypes 중 하나를 변경</span><span class="sxs-lookup"><span data-stu-id="03e91-739">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="03e91-740">목록\<DataLakeAnalyticsAccount> 목록\<PSDataLakeAnalyticsAccountBasic>으로</span><span class="sxs-lookup"><span data-stu-id="03e91-740">List\<DataLakeAnalyticsAccount> to List\<PSDataLakeAnalyticsAccountBasic></span></span>
    - <span data-ttu-id="03e91-741">PSDataLakeAnalyticsAccountBasic의 속성은 DataLakeAnalyticsAccount 속성의 엄격한 하위 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-741">The properties of PSDataLakeAnalyticsAccountBasic is a strict subset of the properties of DataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="03e91-742">DataLakeAnalyticsAccount에 있는 추가 속성은 서비스에 의해 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-742">The additional properties that are in DataLakeAnalyticsAccount are not returned by the service.</span></span>  <span data-ttu-id="03e91-743">따라서 이 변경 사항은 이를 정확하게 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-743">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="03e91-744">이러한 추가 속성은 PSDataLakeAnalyticsAccountBasic에 여전히 있지만, Obsolete로 태그가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-744">These additional properties are still in PSDataLakeAnalyticsAccountBasic, but they are tagged as Obsolete.</span></span>
  * <span data-ttu-id="03e91-745">Get-AzureRmDataLakeAnalyticsJob의 두 가지 OutputTypes 중 하나를 변경</span><span class="sxs-lookup"><span data-stu-id="03e91-745">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="03e91-746">목록\<JobInformation> 목록\<PSJobInformationBasic>으로</span><span class="sxs-lookup"><span data-stu-id="03e91-746">List\<JobInformation> to List\<PSJobInformationBasic></span></span>
    - <span data-ttu-id="03e91-747">PSJobInformationBasic 속성은 JobInformation 속성의 엄격한 하위 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-747">The properties of PSJobInformationBasic is a strict subset of the properties of JobInformation</span></span>
    - <span data-ttu-id="03e91-748">JobInformation에 있는 추가 속성은 서비스에 의해 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-748">The additional properties that are in JobInformation are not returned by the service.</span></span>  <span data-ttu-id="03e91-749">따라서 이 변경 사항은 이를 정확하게 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-749">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="03e91-750">이러한 추가 속성은 PSJobInformationBasic에 여전히 있지만, Obsolete로 태그가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-750">These additional properties are still in PSJobInformationBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="03e91-751">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="03e91-751">DataLakeStore</span></span>
  * <span data-ttu-id="03e91-752">이 릴리스의 DataLakeStore에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-752">Please see the migration guide for breaking changes made to DataLakeStore this release</span></span>
  * <span data-ttu-id="03e91-753">Get-AzureRmDataLakeStoreAccount의 두 가지 OutputTypes 중 하나를 변경</span><span class="sxs-lookup"><span data-stu-id="03e91-753">Changed one of the two OutputTypes of Get-AzureRmDataLakeStoreAccount</span></span>
    - <span data-ttu-id="03e91-754">목록\<PSDataLakeStoreAccount> 목록\<PSDataLakeStoreAccountBasic>으로</span><span class="sxs-lookup"><span data-stu-id="03e91-754">List\<PSDataLakeStoreAccount> to List\<PSDataLakeStoreAccountBasic></span></span>
    - <span data-ttu-id="03e91-755">PSDataLakeStoreAccountBasic의 속성은 PSDataLakeStoreAccount 속성의 엄격한 하위 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-755">The properties of PSDataLakeStoreAccountBasic is a strict subset of the properties of PSDataLakeStoreAccount</span></span>
    - <span data-ttu-id="03e91-756">PSDataLakeStoreAccount에 있는 추가 속성은 서비스에 의해 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-756">The additional properties that are in PSDataLakeStoreAccount are not returned by the service.</span></span>  <span data-ttu-id="03e91-757">따라서 이 변경 사항은 이를 정확하게 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-757">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="03e91-758">이러한 추가 속성은 PSDataLakeStoreAccountBasic에 여전히 있지만, Obsolete로 태그가 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-758">These additional properties are still in PSDataLakeStoreAccountBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="03e91-759">Dns</span><span class="sxs-lookup"><span data-stu-id="03e91-759">Dns</span></span>
  * <span data-ttu-id="03e91-760">Azure DNS의 CAA 레코드 종류에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-760">Support for CAA record types in Azure DNS</span></span>
    - <span data-ttu-id="03e91-761">CAA 레코드 종류에서 모든 작업 지원</span><span class="sxs-lookup"><span data-stu-id="03e91-761">Supports all operations on CAA record type</span></span>
* <span data-ttu-id="03e91-762">EventHub</span><span class="sxs-lookup"><span data-stu-id="03e91-762">EventHub</span></span>
  * <span data-ttu-id="03e91-763">이 릴리스의 EventHub에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-763">Please see the migration guide for breaking changes made to EventHub this release</span></span>
* <span data-ttu-id="03e91-764">자세한 정보</span><span class="sxs-lookup"><span data-stu-id="03e91-764">Insights</span></span>
  * <span data-ttu-id="03e91-765">이 릴리스의 Insights에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-765">Please see the migration guide for breaking changes made to Insights this release</span></span>
* <span data-ttu-id="03e91-766">네트워크</span><span class="sxs-lookup"><span data-stu-id="03e91-766">Network</span></span>
  * <span data-ttu-id="03e91-767">이 릴리스의 Network에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-767">Please see the migration guide for breaking changes made to Network this release</span></span>
  * <span data-ttu-id="03e91-768">지정된 Azure 지역에 대해 사용 가능한 인터넷 서비스 공급자를 나열하는 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-768">Added cmdlet to list available internet service providers for a specified Azure region</span></span>
    - <span data-ttu-id="03e91-769">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="03e91-769">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>
  * <span data-ttu-id="03e91-770">지정된 위치에서 Azure 지역까지 인터넷 서비스 공급자에 대한 상대적 대기 시간 점수를 얻기 위한 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-770">Added cmdlet to get the relative latency score for internet service providers from a specified location to Azure regions</span></span>
    - <span data-ttu-id="03e91-771">Get-AzureRmNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="03e91-771">Get-AzureRmNetworkWatcherReachabilityReport</span></span>
* <span data-ttu-id="03e91-772">프로필</span><span class="sxs-lookup"><span data-stu-id="03e91-772">Profile</span></span>
  - <span data-ttu-id="03e91-773">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="03e91-773">Set-AzureRmDefault</span></span>
    - <span data-ttu-id="03e91-774">이 cmdlet을 사용하여 기본 리소스 그룹을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-774">Use this cmdlet to set a default resource group.</span></span>  <span data-ttu-id="03e91-775">이렇게 하면 일부 cmdlet에 대해 -ResourceGroup 매개 변수가 선택 사항이 되고 리소스 그룹이 지정되지 않은 경우 기본값이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-775">This will make the -ResourceGroup parameter optional for some cmdlets, and will use the default when a resource group is not specified</span></span>
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - <span data-ttu-id="03e91-776">구독에 지정된 리소스 그룹이 있으면 이 리소스 그룹은 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-776">If resource group specified exists in the subscription, this resource group will be set to default.</span></span>  <span data-ttu-id="03e91-777">그렇지 않은 경우 리소스 그룹이 만들어진 다음 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-777">Otherwise, the resource group will be created and then set to default.</span></span>
  - <span data-ttu-id="03e91-778">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="03e91-778">Get-AzureRmDefault</span></span>
    - <span data-ttu-id="03e91-779">이 cmdlet을 사용하여 현재 기본 리소스 그룹(및 나중의 다른 기본값)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-779">Use this cmdlet to get the current default resource group (and other defaults in the future).</span></span>
    - ```Get-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="03e91-780">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="03e91-780">Clear-AzureRmDefault</span></span>
    - <span data-ttu-id="03e91-781">이 cmdlet을 사용하여 현재 기본 리소스 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-781">Use this cmdlet to remove the current default resource group</span></span>
    - ```Clear-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="03e91-782">Add-AzureRmEnvironment 및 Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="03e91-782">Add-AzureRmEnvironment and Set-AzureRmEnvironment</span></span>
    - <span data-ttu-id="03e91-783">일괄 처리 서비스에 대한 인증 토큰을 얻을 때 사용할 Azure Batch Active Directory 대상을 지정할 수 있는 BatchAudience 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-783">Add the BatchAudience parameter, which allows you to specify the Azure Batch Active Directory audience to use when acquiring authentication tokens for the Batch service.</span></span>
* <span data-ttu-id="03e91-784">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="03e91-784">RecoveryServices.Backup</span></span>
  * <span data-ttu-id="03e91-785">즉시 파일 복구를 수행하기 위해 cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-785">Added cmdlets to perform instant file recovery.</span></span>
    - <span data-ttu-id="03e91-786">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="03e91-786">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>
    - <span data-ttu-id="03e91-787">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="03e91-787">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>
  * <span data-ttu-id="03e91-788">RecoveryServices.Backup SDK 버전을 최신 버전으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="03e91-788">Updated RecoveryServices.Backup SDK version to the latest</span></span>
  * <span data-ttu-id="03e91-789">테스트 실행에 필요한 모든 설정이 테스트 자체에서 지정되도록 Azure VM 워크로드에 대한 테스트를 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-789">Updated tests for the Azure VM workload so that, all setups needed for test runs are done by the tests themselves.</span></span>
  * <span data-ttu-id="03e91-790">https://github.com/Azure/azure-powershell/issues/3164 수정</span><span class="sxs-lookup"><span data-stu-id="03e91-790">Fixes https://github.com/Azure/azure-powershell/issues/3164</span></span>
* <span data-ttu-id="03e91-791">RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="03e91-791">RecoveryServices.SiteRecovery</span></span>
  * <span data-ttu-id="03e91-792">ASR VMware의 Azure Site Recovery에 대한 변경 사항(cmdlet은 현재 Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure에 대한 작업을 지원)</span><span class="sxs-lookup"><span data-stu-id="03e91-792">Changes for ASR VMware to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure)</span></span>
    - <span data-ttu-id="03e91-793">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="03e91-793">New-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="03e91-794">New-AzureRmRecoveryServicesAsrProtectedItem</span><span class="sxs-lookup"><span data-stu-id="03e91-794">New-AzureRmRecoveryServicesAsrProtectedItem</span></span>
    - <span data-ttu-id="03e91-795">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="03e91-795">Update-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="03e91-796">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="03e91-796">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>
  * <span data-ttu-id="03e91-797">AAD 기반 자격 증명 모음에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-797">Added support to AAD-based vault</span></span>
  * <span data-ttu-id="03e91-798">VCenter 리소스를 관리하기 위해 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="03e91-798">Added cmdlets to manage VCenter resources</span></span>
    - <span data-ttu-id="03e91-799">Get-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="03e91-799">Get-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="03e91-800">New-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="03e91-800">New-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="03e91-801">Remove-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="03e91-801">Remove-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="03e91-802">Update-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="03e91-802">Update-AzureRmRecoveryServicesAsrVCenter</span></span>
  * <span data-ttu-id="03e91-803">다른 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-803">Added other cmdlets</span></span>
    - <span data-ttu-id="03e91-804">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="03e91-804">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="03e91-805">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="03e91-805">Get-AzureRmRecoveryServicesAsrEvent</span></span>
    - <span data-ttu-id="03e91-806">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="03e91-806">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
    - <span data-ttu-id="03e91-807">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="03e91-807">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="03e91-808">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="03e91-808">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>
    - <span data-ttu-id="03e91-809">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="03e91-809">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>
    - <span data-ttu-id="03e91-810">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="03e91-810">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>
    - <span data-ttu-id="03e91-811">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="03e91-811">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>
* <span data-ttu-id="03e91-812">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="03e91-812">ServiceBus</span></span>
  - <span data-ttu-id="03e91-813">이 릴리스의 ServiceBus에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e91-813">Please see the migration guide for breaking changes made to ServiceBus this release</span></span>
* <span data-ttu-id="03e91-814">Sql</span><span class="sxs-lookup"><span data-stu-id="03e91-814">Sql</span></span>
  * <span data-ttu-id="03e91-815">목록에 대한 지원 추가 및 데이터베이스에서 비동기 updatelo 작업 취소</span><span class="sxs-lookup"><span data-stu-id="03e91-815">Adding support for list and cancel the asynchronous updateslo operation on the database</span></span>
    - <span data-ttu-id="03e91-816">기존 cmdlet Get-AzureRmSqlDatabaseActivity를 업데이트하여 DB updateslo를 작업 상태로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-816">update existing cmdlet Get-AzureRmSqlDatabaseActivity to return DB updateslo operation status.</span></span>
    - <span data-ttu-id="03e91-817">새 cmdlet Stop-AzureRmSqlDatabaseActivity를 추가하여 데이터베이스에서 비동기 updateslo 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="03e91-817">add new cmdlet Stop-AzureRmSqlDatabaseActivity for cancel the asynchronous updateslo operation on the database.</span></span>
  * <span data-ttu-id="03e91-818">데이터베이스 및 탄성 풀에 대한 영역 중복 지원 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-818">Adding support for Zone Redundancy for databases and elastic pools</span></span>
    - <span data-ttu-id="03e91-819">New-AzureRmSqlDatabase에 ZoneRedundant 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-819">Adding ZoneRedundant switch parameter to New-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="03e91-820">Set-AzureRmSqlDatabase에 ZoneRedundant 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-820">Adding ZoneRedundant switch parameter to Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="03e91-821">New-AzureRmSqlElasticPool에 ZoneRedundant 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-821">Adding ZoneRedundant switch parameter to New-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="03e91-822">Set-AzureRmSqlElasticPool에 ZoneRedundant 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-822">Adding ZoneRedundant switch parameter to Set-AzureRmSqlElasticPool</span></span>
  * <span data-ttu-id="03e91-823">서버 DNS 별칭에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-823">Adding support for Server DNS Aliases</span></span>
    - <span data-ttu-id="03e91-824">서버 및 별칭 이름별 서버 DNS 별칭 또는 Azure SQL Server에 대한 서버 DNS 별칭의 목록을 가져오는 Get-AzureRmSqlServerDnsAlias cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-824">Adding Get-AzureRmSqlServerDnsAlias cmdlet which gets server dns aliases by server and alias name or a list of server dns aliases for an azure Sql Server.</span></span>
    - <span data-ttu-id="03e91-825">지정된 Azure SQL Server에 대한 새 서버 DNS 별칭을 만드는 New-AzureRmSqlServerDnsAlias cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-825">Adding New-AzureRmSqlServerDnsAlias cmdlet which creates new server dns alias for a given Azure Sql server</span></span>
    - <span data-ttu-id="03e91-826">서버 DNS 별칭이 가리키는 Azure SQL Server의 업데이트를 허용하는 Set-AzurermSqlServerDnsAlias cmlet 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-826">Adding Set-AzurermSqlServerDnsAlias cmlet which allows updating a Azure Sql Server to which server dns alias is pointing</span></span>
    - <span data-ttu-id="03e91-827">Azure SQL Server에 대한 새 서버 DNS 별칭을 제거하는 Remove-AzureRmSqlServerDnsAlias cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-827">Adding Remove-AzureRmSqlServerDnsAlias cmdlet which removes a server dns alias for a Azure Sql Server</span></span>
* <span data-ttu-id="03e91-828">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="03e91-828">Azure.Storage</span></span>
  * <span data-ttu-id="03e91-829">Azure Storage 클라이언트 라이브러리 8.5.0 및 Azure Storage DataMovement 라이브러리 0.6.3으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="03e91-829">Upgrade to Azure Storage Client Library 8.5.0 and Azure Storage DataMovement Library 0.6.3</span></span>
  * <span data-ttu-id="03e91-830">파일 공유 스냅숏 지원 기능 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-830">Add File Share Snapshot Support Feature</span></span>
    - <span data-ttu-id="03e91-831">Get-AzureStorageShare에 'SnapshotTime' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-831">Add 'SnapshotTime' parameter to Get-AzureStorageShare</span></span>
    - <span data-ttu-id="03e91-832">Remove-AzureStorageShare에 'IncludeAllSnapshot' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="03e91-832">Add 'IncludeAllSnapshot' parameter to Remove-AzureStorageShare</span></span>
