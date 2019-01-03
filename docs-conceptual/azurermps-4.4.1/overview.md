---
title: Azure PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 링크를 포함한 Azure PowerShell 개요입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: 5ee8572ccb8e9fc2de11c2253a1815a666e038a7
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736498"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="74b99-103">Azure PowerShell 개요</span><span class="sxs-lookup"><span data-stu-id="74b99-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="74b99-104">Azure PowerShell은 Azure 리소스를 관리하기 위해 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 모델을 사용하는 cmdlet 집합을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="74b99-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="74b99-105">[Azure Cloud Shell](/azure/cloud-shell/overview)과 함께 브라우저에서 사용하거나 로컬 컴퓨터에 설치하여 PowerShell 세션에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b99-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="74b99-106">[Cloud Shell](/azure/cloud-shell/overview)을 사용하여 브라우저에서 Azure PowerShell을 실행하거나 자신의 컴퓨터에 [설치](install-azurerm-ps.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="74b99-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="74b99-107">그런 다음 [시작](get-started-azureps.md) 문서를 읽고 사용을 시작해 보세요.</span><span class="sxs-lookup"><span data-stu-id="74b99-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="74b99-108">최신 릴리스에 대한 자세한 내용은 [릴리스 정보](release-notes-azureps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74b99-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="74b99-109">다음 샘플을 통해 Azure PowerShell로 일반 시나리오를 수행하는 방법을 배울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b99-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="74b99-110">Linux Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="74b99-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="74b99-111">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="74b99-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="74b99-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="74b99-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="74b99-113">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="74b99-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="74b99-114">PowerShell 기본 사항 알아보기</span><span class="sxs-lookup"><span data-stu-id="74b99-114">Learn PowerShell basics</span></span>

<span data-ttu-id="74b99-115">PowerShell에 대해 잘 모른다면 PowerShell에 대한 소개가 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b99-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="74b99-116">PowerShell 설치</span><span class="sxs-lookup"><span data-stu-id="74b99-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="74b99-117">PowerShell 스크립팅</span><span class="sxs-lookup"><span data-stu-id="74b99-117">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="74b99-118">이 비디오를 시청할 수도 있습니다. [PowerShell 기본 사항: (파트 1)PowerShell 시작](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)</span><span class="sxs-lookup"><span data-stu-id="74b99-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="74b99-119">또는 Microsoft Virtual Academy의 [PowerShell 시작](https://mva.microsoft.com/liveevents/powershell-jumpstart)에 참석합니다.</span><span class="sxs-lookup"><span data-stu-id="74b99-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="74b99-120">다른 Azure PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="74b99-120">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="74b99-121">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="74b99-121">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="74b99-122">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="74b99-122">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="74b99-123">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="74b99-123">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="74b99-124">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="74b99-124">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
