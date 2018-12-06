---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826657"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="b2c96-103">Azure Stack 모듈 1.4.0</span><span class="sxs-lookup"><span data-stu-id="b2c96-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c96-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="b2c96-104">Requirements:</span></span>
<span data-ttu-id="b2c96-105">최소 지원 Azure Stack 버전은 1804입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="b2c96-106">참고: 이전 버전을 사용하는 경우 1.2.11 버전을 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="b2c96-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="b2c96-107">알려진 문제:</span><span class="sxs-lookup"><span data-stu-id="b2c96-107">Known issues:</span></span>

- <span data-ttu-id="b2c96-108">경고 닫기에는 Azure Stack 버전 1803이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="b2c96-109">New-AzsOffer는 상태를 공개하여 제안을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="b2c96-110">상태를 변경하려면 Set-AzsOffer cmdlet을 나중에 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="b2c96-111">재배포하지 않고는 IP 풀을 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="b2c96-112">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="b2c96-112">Breaking Changes</span></span>
<span data-ttu-id="b2c96-113">버전 1.3.0과 호환성이 손상되는 변경은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="b2c96-114">1.2.11에서 마이그레이션하는 호환성이 손상되는 변경은 모두 여기 https://aka.ms/azspowershellmigration에 문서화되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="b2c96-115">설치</span><span class="sxs-lookup"><span data-stu-id="b2c96-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="b2c96-116">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="b2c96-116">Release Notes</span></span>
    * <span data-ttu-id="b2c96-117">Azurestack 1.4.0 버전에는 이전 버전인 1.3.0과 호환성이 손상되는 변경은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="b2c96-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="b2c96-119">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="b2c96-121">새 매개 변수 BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays를 Set-AzsBackupShare cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="b2c96-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="b2c96-122">암호화 키 만들기를 용이하게 하기 위해 New-EncyptionKeyBase64 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="b2c96-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="b2c96-123">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="b2c96-125">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="b2c96-127">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="b2c96-128">azurestack 스탬프에 새 배율 단위 노드를 추가하는 관리자를 활성화하는 Add-AzsScaleUnitNode cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="b2c96-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="b2c96-129">배율 단위 매개 변수 개체 생성을 용이하게 하기 위해 cmdlet 및 New-AzsScaleUnitNodeObject 추가</span><span class="sxs-lookup"><span data-stu-id="b2c96-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="b2c96-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="b2c96-131">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="b2c96-133">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="b2c96-135">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="b2c96-137">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="b2c96-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="b2c96-139">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="b2c96-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="b2c96-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="b2c96-141">위임된 공급자 제안 간에 구독을 이동하기 위한 Move-AzsSubscription cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="b2c96-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="b2c96-142">사용자 구독이 위임된 공급자 제품 간에 이동할 수 있는지 유효성 검사를 하기 위해 Test-AzsMoveSubscription cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="b2c96-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="b2c96-143">페이지가 매겨진 결과 내에서 단일 페이지만 반환하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="b2c96-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="b2c96-144">콘텐츠:</span><span class="sxs-lookup"><span data-stu-id="b2c96-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="b2c96-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="b2c96-145">Azure Bridge</span></span>
<span data-ttu-id="b2c96-146">Azure의 이미지를 배포할 수 있게 해주는 Azure Stack AzureBridge 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="b2c96-147">Backup</span><span class="sxs-lookup"><span data-stu-id="b2c96-147">Backup</span></span>
<span data-ttu-id="b2c96-148">관리자가 다음을 수행할 수 있도록 해주는 Backup 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="b2c96-149">백업이 저장되는 위치 구성</span><span class="sxs-lookup"><span data-stu-id="b2c96-149">Configure where backups are stored</span></span>
- <span data-ttu-id="b2c96-150">백업 수행</span><span class="sxs-lookup"><span data-stu-id="b2c96-150">Perform backups</span></span>
- <span data-ttu-id="b2c96-151">완료된 백업 나열 및 복원</span><span class="sxs-lookup"><span data-stu-id="b2c96-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="b2c96-152">상거래</span><span class="sxs-lookup"><span data-stu-id="b2c96-152">Commerce</span></span>
<span data-ttu-id="b2c96-153">Azure Stack 시스템의 집계 데이터 사용량을 볼 수 있는 방법을 제공하는 Azure Stack Commerce 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="b2c96-154">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="b2c96-154">Compute</span></span>
<span data-ttu-id="b2c96-155">컴퓨팅 할당량, 플랫폼 이미지 및 가상 컴퓨터 확장을 관리하는 기능을 제공하는 Azure Stack Compute 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="b2c96-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="b2c96-156">Fabric</span></span>
<span data-ttu-id="b2c96-157">관리자가 다음 작업을 위해 인프라 구성 요소를 보고 관리할 수 있게 해주는 Azure Stack Fabric 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="b2c96-158">배율 단위 노드의 중지, 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="b2c96-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="b2c96-159">FRU 관련 활동에 대한 배율 단위 노드의 배출 및 재개</span><span class="sxs-lookup"><span data-stu-id="b2c96-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="b2c96-160">배율 단위 노드의 복구</span><span class="sxs-lookup"><span data-stu-id="b2c96-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="b2c96-161">인프라 역할의 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b2c96-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="b2c96-162">인프라 역할 인스턴스의 중지, 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="b2c96-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="b2c96-163">새 IP 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="b2c96-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="b2c96-164">갤러리</span><span class="sxs-lookup"><span data-stu-id="b2c96-164">Gallery</span></span>
<span data-ttu-id="b2c96-165">Azure Stack Marketplace에서 갤러리 항목을 관리하는 기능을 제공하는 Azure Stack Gallery 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="b2c96-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="b2c96-166">Infrastructure Insights</span></span>
<span data-ttu-id="b2c96-167">관리자가 다음을 수행할 수 있는 Infrastructure Insight 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="b2c96-168">Azure Stack 스탬프 리소스의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="b2c96-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="b2c96-169">경고 보기 및 관리</span><span class="sxs-lookup"><span data-stu-id="b2c96-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="b2c96-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b2c96-170">KeyVault</span></span>
<span data-ttu-id="b2c96-171">관리자가 KeyVault 할당량을 볼 수 있는 Azure Stack KeyVault 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="b2c96-172">네트워크</span><span class="sxs-lookup"><span data-stu-id="b2c96-172">Network</span></span>
<span data-ttu-id="b2c96-173">다음을 수행할 수 있는 Network 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="b2c96-174">네트워크 할당량 관리</span><span class="sxs-lookup"><span data-stu-id="b2c96-174">Management of network quotas</span></span>
- <span data-ttu-id="b2c96-175">공용 IP 주소, 가상 네트워크, 부하 분산 장치와 같은 할당된 네트워크 리소스 보기</span><span class="sxs-lookup"><span data-stu-id="b2c96-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="b2c96-176">관리자 개요를 표시하는 cmdlet을 제공</span><span class="sxs-lookup"><span data-stu-id="b2c96-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="b2c96-177">Storage</span><span class="sxs-lookup"><span data-stu-id="b2c96-177">Storage</span></span>
<span data-ttu-id="b2c96-178">Azure Stack Storage 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="b2c96-179">이 릴리스에서는 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="b2c96-180">저장소 할당량 관리</span><span class="sxs-lookup"><span data-stu-id="b2c96-180">Manage storage quotas</span></span>
- <span data-ttu-id="b2c96-181">삭제된 저장소 리소스 가비지 수집</span><span class="sxs-lookup"><span data-stu-id="b2c96-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="b2c96-182">삭제된 저장소 계정 복원</span><span class="sxs-lookup"><span data-stu-id="b2c96-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="b2c96-183">한 공유에서 다른 공유로 컨테이너 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="b2c96-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="b2c96-184">개별 저장소 구성 요소에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="b2c96-184">View information about the individual storage components</span></span>
- <span data-ttu-id="b2c96-185">사용량 및 성능 정보 보기</span><span class="sxs-lookup"><span data-stu-id="b2c96-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="b2c96-186">구독 관리자</span><span class="sxs-lookup"><span data-stu-id="b2c96-186">Subscription Admin</span></span>
<span data-ttu-id="b2c96-187">Azure Stack Subscription 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="b2c96-188">이 모듈은 관리자가 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="b2c96-189">계획 및 제안 관리</span><span class="sxs-lookup"><span data-stu-id="b2c96-189">Manage plans and offers</span></span>
- <span data-ttu-id="b2c96-190">사용량 및 성능 정보 보기</span><span class="sxs-lookup"><span data-stu-id="b2c96-190">View usage and performance information</span></span>
- <span data-ttu-id="b2c96-191">RBAC 관리</span><span class="sxs-lookup"><span data-stu-id="b2c96-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="b2c96-192">구독</span><span class="sxs-lookup"><span data-stu-id="b2c96-192">Subscription</span></span>
<span data-ttu-id="b2c96-193">Azure Stack Subscription 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="b2c96-194">이 모듈은 사용자가 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="b2c96-195">구독 생성, 삭제 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="b2c96-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="b2c96-196">주 지역에서</span><span class="sxs-lookup"><span data-stu-id="b2c96-196">Update</span></span>
<span data-ttu-id="b2c96-197">Azure Stack Update 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="b2c96-198">이 모듈에서 관리자는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2c96-198">In this module administrators can:</span></span>
- <span data-ttu-id="b2c96-199">사용 가능한 업데이트 나열 및 설치</span><span class="sxs-lookup"><span data-stu-id="b2c96-199">List and install available updates</span></span>
- <span data-ttu-id="b2c96-200">중단된 업데이트 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b2c96-200">Resume interrupted updates</span></span>
- <span data-ttu-id="b2c96-201">설치된 업데이트 보기</span><span class="sxs-lookup"><span data-stu-id="b2c96-201">View installed updates</span></span>
