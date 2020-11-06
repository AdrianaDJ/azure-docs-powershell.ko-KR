---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537668"
---
# <span data-ttu-id="0241c-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0241c-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="0241c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0241c-102">SYNOPSIS</span></span>
<span data-ttu-id="0241c-103">알림 허브 네임 스페이스와 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0241c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0241c-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0241c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0241c-105">DESCRIPTION</span></span>
<span data-ttu-id="0241c-106">**AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet은 알림 허브 네임 스페이스와 관련 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="0241c-107">네임 스페이스와 관련 된 모든 규칙에 대 한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="0241c-108">또는 *authorizationrule* 매개 변수를 포함 하 여 특정 규칙에 대 한 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="0241c-109">권한 부여 규칙은 네임 스페이스에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="0241c-110">이 작업은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="0241c-111">플랫폼 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="0241c-112">듣기</span><span class="sxs-lookup"><span data-stu-id="0241c-112">Listen</span></span>
- <span data-ttu-id="0241c-113">보내기</span><span class="sxs-lookup"><span data-stu-id="0241c-113">Send</span></span>
- <span data-ttu-id="0241c-114">관리자</span><span class="sxs-lookup"><span data-stu-id="0241c-114">Manage</span></span>

<span data-ttu-id="0241c-115">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="0241c-116">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 사용 권한에 대 한 URI로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="0241c-117">이 cmdlet은 네임 스페이스와 관련 된 권한 부여 규칙만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="0241c-118">네임 스페이스 자체에 대 한 정보를 얻으려면 Get-AzureRmNotificationHubsNamespace를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="0241c-119">예제의</span><span class="sxs-lookup"><span data-stu-id="0241c-119">EXAMPLES</span></span>

### <span data-ttu-id="0241c-120">예제 1: 네임 스페이스에 할당 된 모든 권한 부여 규칙에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0241c-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="0241c-121">이 명령은 네임 스페이스 ContosoNamespace 및 ContosoNotificationsGroup 리소스 그룹에 모두 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="0241c-122">예제 2: 권한 부여 규칙에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0241c-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="0241c-123">이 명령은 ListenRule 이라는 단일 네임 스페이스 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="0241c-124">특정 권한 부여 규칙에 대 한 정보를 가져올 때는 네임 스페이스와 리소스 그룹을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="0241c-125">변수</span><span class="sxs-lookup"><span data-stu-id="0241c-125">PARAMETERS</span></span>

### <span data-ttu-id="0241c-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0241c-126">-AuthorizationRule</span></span>
<span data-ttu-id="0241c-127">SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="0241c-128">이러한 규칙은 네임 스페이스에 대 한 사용자의 액세스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-128">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0241c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0241c-129">-DefaultProfile</span></span>
<span data-ttu-id="0241c-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0241c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0241c-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0241c-131">-Namespace</span></span>
<span data-ttu-id="0241c-132">권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-132">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="0241c-133">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-133">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0241c-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0241c-134">-ResourceGroup</span></span>
<span data-ttu-id="0241c-135">권한 부여 규칙이 할당 되는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-135">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="0241c-136">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-136">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0241c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0241c-137">CommonParameters</span></span>
<span data-ttu-id="0241c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0241c-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0241c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0241c-140">입력</span><span class="sxs-lookup"><span data-stu-id="0241c-140">INPUTS</span></span>

### <span data-ttu-id="0241c-141">않아야</span><span class="sxs-lookup"><span data-stu-id="0241c-141">None</span></span>
<span data-ttu-id="0241c-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0241c-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0241c-143">출력</span><span class="sxs-lookup"><span data-stu-id="0241c-143">OUTPUTS</span></span>

### <span data-ttu-id="0241c-144">System.webserver. List ' 1 [Microsoft Azure. 명령. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="0241c-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="0241c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0241c-145">NOTES</span></span>

## <span data-ttu-id="0241c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0241c-146">RELATED LINKS</span></span>

[<span data-ttu-id="0241c-147">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0241c-147">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="0241c-148">새로운 AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0241c-148">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="0241c-149">제거-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0241c-149">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="0241c-150">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0241c-150">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)

