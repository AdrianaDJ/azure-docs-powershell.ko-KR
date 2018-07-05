---
title: PowerShell 세션간에 사용자 자격 증명 유지
description: 여러 PowerShell 세션에 걸쳐 Azure 자격 증명 및 다른 정보를 재사용하는 방법에 대해 알아보세요.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: aa374c6e93124fb4b428aa8c4854f7424f494bff
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091353"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="26680-103">PowerShell 세션에 걸쳐 사용자 자격 증명 유지</span><span class="sxs-lookup"><span data-stu-id="26680-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="26680-104">Azure PowerShell의 2017년 9월 릴리스에서 Azure Resource Manager cmdlet은 새로운 기능인 **Azure 컨텍스트 자동 저장**을 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="26680-105">이 기능을 통해 다음을 비롯한 여러 새로운 사용자 시나리오를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="26680-106">새 PowerShell 세션에서 다시 사용하기 위한 로그인 정보 보존.</span><span class="sxs-lookup"><span data-stu-id="26680-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="26680-107">장기 실행 cmdlet을 실행하기 위한 더 쉬운 백그라운드 작업 사용.</span><span class="sxs-lookup"><span data-stu-id="26680-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="26680-108">별도 로그인 없이 계정, 구독 및 환경 간 전환.</span><span class="sxs-lookup"><span data-stu-id="26680-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="26680-109">동일한 PowerShell 세션에서 다른 자격 증명 및 구독을 동시에 사용하여 작업 실행.</span><span class="sxs-lookup"><span data-stu-id="26680-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="26680-110">정의된 Azure 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="26680-110">Azure contexts defined</span></span>

<span data-ttu-id="26680-111">*Azure 컨텍스트*는 Azure PowerShell cmdlet의 대상을 정의하는 정보 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="26680-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="26680-112">컨텍스트는 5개의 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="26680-112">The context consists of five parts:</span></span>

- <span data-ttu-id="26680-113">*계정* - Azure와의 통신을 인증하는 데 사용되는 사용자 이름 또는 서비스 주체</span><span class="sxs-lookup"><span data-stu-id="26680-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="26680-114">*구독* - 동작하는 리소스를 포함하는 Azure 구독.</span><span class="sxs-lookup"><span data-stu-id="26680-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="26680-115">*테넌트* - 구독을 포함하는 Azure Active Directory 테넌트.</span><span class="sxs-lookup"><span data-stu-id="26680-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="26680-116">테넌트는 ServicePrincipal 인증에서 더 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="26680-117">*환경* - 목표가 되는 특정 Azure Cloud(보통 Azure 전역 클라우드).</span><span class="sxs-lookup"><span data-stu-id="26680-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="26680-118">그러나 환경 설정을 사용하여 대상 국가, 정부 및 온-프레미스(Azure Stack) 클라우드도 대상으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="26680-119">*자격 증명* - Azure에서 사용자 ID를 확인하고 Azure의 리소스에 액세스하기 위한 사용자의 권한 부여를 확인하는 데 사용되는 정보</span><span class="sxs-lookup"><span data-stu-id="26680-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="26680-120">이전 릴리스에서는 새 PowerShell 세션을 열 때마다 Azure 컨텍스트를 만들어야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="26680-121">Azure PowerShell v4.4.0부터는 새 PowerShell 세션을 열 때 언제든지 Azure 컨텍스트의 자동 저장 및 다시 사용을 활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="26680-122">다음 로그인을 위해 컨텍스트를 자동으로 저장</span><span class="sxs-lookup"><span data-stu-id="26680-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="26680-123">기본적으로 Azure PowerShell은 PowerShell 세션을 닫을 때마다 컨텍스트 정보를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="26680-124">Azure PowerShell이 PowerShell 세션을 닫은 후 사용자의 컨텍스트를 기억하도록 하려면 `Enable-AzureRmContextAutosave`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="26680-125">컨텍스트 및 자격 증명 정보는 사용자 디렉터리(`%AppData%\Roaming\Windows Azure PowerShell`)에 숨겨진 특수 폴더에 자동으로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="26680-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="26680-126">그 후 새로운 PowerShell 세션마다 마지막 세션에 사용된 컨텍스트를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="26680-127">PowerShell이 사용자의 컨텍스트 및 자격 증명을 기억하지 않도록 설정하려면 `Disable-AzureRmContextAutoSave`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="26680-128">PowerShell 세션을 열 때마다 Azure에 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="26680-129">Azure 컨텍스트를 관리할 수 있는 cmdlet을 사용하면 세분화된 제어가 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="26680-130">변경 내용을 현재 PowerShell 세션(`Process` 범위)에만 적용하거나 또는 모든 PowerShell 세션(`CurrentUser` 범위)에 적용하려는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="26680-131">이러한 옵션은 [컨텍스트 범위 사용](#Using-Context-Scopes)에서 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="26680-132">Azure PowerShell cmdlet을 백그라운드 작업으로 실행</span><span class="sxs-lookup"><span data-stu-id="26680-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="26680-133">**Azure 컨텍스트 자동 저장** 기능을 사용하면 PowerShell 백그라운드 작업으로 컨텍스트를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="26680-134">PowerShell을 사용하면 장기 실행 작업을 작업이 완료될 때까지 기다리지 않고 백그라운드 작업으로 시작하고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="26680-135">두 가지 방법으로 백그라운드 작업으로 자격 증명을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="26680-136">컨텍스트를 인수로 전달</span><span class="sxs-lookup"><span data-stu-id="26680-136">Passing the context as an argument</span></span>

  <span data-ttu-id="26680-137">대부분 AzureRM cmdlet을 사용하면 cmdlet에 컨텍스트를 매개 변수로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="26680-138">다음 예제와 같이 백그라운드 작업으로 컨텍스트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="26680-139">자동 저장이 활성화된 기본 컨텍스트 사용</span><span class="sxs-lookup"><span data-stu-id="26680-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="26680-140">**컨텍스트 자동 저장**을 사용하도록 설정한 경우 백그라운드 작업은 자동으로 기본 저장된 기본 컨텍스트를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="26680-141">백그라운드 작업의 결과를 알아야 하는 경우 `Get-Job`을 사용하여 작업 상태를 확인하고 `Wait-Job`을 사용하여 작업이 완료될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="26680-142">백그라운드 작업의 출력을 캡처하거나 표시하려면 `Receive-Job`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="26680-143">자세한 내용은 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="26680-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="26680-144">컨텍스트 생성, 선택, 이름 바꾸기 및 제거</span><span class="sxs-lookup"><span data-stu-id="26680-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="26680-145">컨텍스트를 작성하려면 Azure에 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="26680-146">`Connect-AzureRmAccount` cmdlet(또는 해당 별칭인 `Login-AzureRmAccount`)은 이후 Azure PowerShell cmdlet에서 사용하는 기본 컨텍스트를 설정하고, 사용자는 이를 통해 로그인 자격 증명에서 허용하는 모든 테넌트 또는 구독에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-146">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="26680-147">로그인한 후 새 컨텍스트를 추가하려면 `Set-AzureRmContext`(또는 해당 별칭인 `Select-AzureRmSubscription`)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="26680-148">앞의 예제는 현재 자격 증명을 사용하여 새 컨텍스트 대상인 ‘Contoso 구독 1’을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="26680-149">새 컨텍스트는 ‘Contoso1’이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="26680-150">컨텍스트에 대한 이름을 제공하지 않은 경우 계정 ID 및 구독 ID를 사용하는 기본 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="26680-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="26680-151">기존 컨텍스트 이름을 바꾸려면 `Rename-AzureRmContext` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="26680-152">예: </span><span class="sxs-lookup"><span data-stu-id="26680-152">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="26680-153">이 예제에서는 자동 이름 `[user1@contoso.org; 123456-7890-1234-564321]`을 사용하는 컨텍스트 이름을 간단한 이름인 ‘Contoso2’로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="26680-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="26680-154">또한 컨텍스트를 관리하는 cmdlet은 신속하게 컨텍스트를 선택할 수 있도록 탭 완성 기능을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="26680-155">마지막으로, 컨텍스트를 제거하려면 `Remove-AzureRmContext` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="26680-156">예: </span><span class="sxs-lookup"><span data-stu-id="26680-156">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="26680-157">‘Contoso2’로 명명된 컨텍스트를 잊었습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="26680-158">이 컨텍스트를 `Set-AzureRmContext`를 사용하여 나중에 다시 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="26680-159">자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="26680-159">Removing credentials</span></span>

<span data-ttu-id="26680-160">`Disconnect-AzureRmAccount`(`Logout-AzureRmAccount`라고도 함)를 사용하여 사용자 또는 서비스 주체에 대한 모든 자격 증명 및 연결된 컨텍스트를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-160">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="26680-161">매개 변수 없이 실행될 때 `Disconnect-AzureRmAccount` cmdlet은 현재 컨텍스트에서 사용자 또는 서비스 주체에 연결된 모든 자격 증명 및 컨텍스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-161">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="26680-162">사용자 이름, 서비스 주체 이름 또는 컨텍스트를 특정 보안 주체를 대상으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="26680-163">컨텍스트 범위 사용</span><span class="sxs-lookup"><span data-stu-id="26680-163">Using context scopes</span></span>

<span data-ttu-id="26680-164">경우에 따라 다른 세션에 영향을 주지 않고 PowerShell 세션에서 컨텍스트를 선택, 변경 또는 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="26680-165">컨텍스트 cmdlet의 기본 동작을 변경하려면 `Scope` 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="26680-166">`Process` 범위는 현재 세션에만 적용되도록 하여 기본 동작을 재정의합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="26680-167">반대로 `CurrentUser` 범위는 현재 세션만이 아닌 모든 세션의 컨텍스트를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="26680-168">예를 들어, 다른 창에 영향을 주지 않고 현재 PowerShell 세션의 기본 컨텍스트 또는 다음에 세션을 열 때 사용되는 컨텍스트를 변경하려면 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="26680-169">컨텍스트 자동 저장 설정이 기억되는 방식</span><span class="sxs-lookup"><span data-stu-id="26680-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="26680-170">컨텍스트 자동 저장 설정은 사용자 Azure PowerShell 디렉터리(`%AppData%\Roaming\Windows Azure PowerShell`)에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="26680-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="26680-171">일부 종류의 컴퓨터 계정은 이 디렉터리에 액세스하지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="26680-172">이러한 시나리오에서 환경 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-172">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="26680-173">‘true’로 설정하면 컨텍스트가 자동으로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="26680-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="26680-174">‘false’로 설정하면 컨텍스트가 저장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="26680-175">AzureRM.Profile 모듈에 대한 변경 내용</span><span class="sxs-lookup"><span data-stu-id="26680-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="26680-176">컨텍스트 관리를 위한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="26680-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="26680-177">[Enable-AzureRmContextAutosave][enable] - powershell 세션 간에 컨텍스트를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="26680-178">변경 내용이 전역 컨텍스트를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="26680-179">[Disable-AzureRmContextAutosave][disable] - 컨텍스트 자동 저장을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="26680-180">새로운 각 PowerShell 세션은 다시 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="26680-181">[Select-AzureRmContext][select] - 기본값으로 컨텍스트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="26680-182">모든 후속 cmdlet이 인증을 위해 이 컨텍스트에서 자격 증명을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="26680-183">[Disconnect-AzureRmAccount][remove-cred] - 계정과 관련된 자격 증명 및 컨텍스트를 모두 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="26680-183">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="26680-184">[Remove-AzureRmContext][remove-context] - 명명된 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="26680-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="26680-185">[Rename-AzureRmContext][rename] - 기존 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="26680-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="26680-186">기존 프로필 cmdlet에 대한 변경 내용</span><span class="sxs-lookup"><span data-stu-id="26680-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="26680-187">[Add-AzureRmAccount][login] - 프로세스 또는 현재 사용자로 로그인의 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="26680-188">로그인한 후 기본 컨텍스트의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="26680-189">[Import-AzureRmContext][import] - 프로세스 또는 현재 사용자로 로그인의 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="26680-190">[Set-AzureRmContext][set-context] - 기존의 명명된 컨텍스트를 선택하고, 프로세스 또는 현재 사용자로 범위를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26680-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
