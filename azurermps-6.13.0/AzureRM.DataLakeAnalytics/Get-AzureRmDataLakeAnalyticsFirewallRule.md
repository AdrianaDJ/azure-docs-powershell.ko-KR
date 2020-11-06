---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 421bf32bd0a3b5a27728c675396c10414c435d84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534380"
---
# <span data-ttu-id="06b9d-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06b9d-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="06b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="06b9d-103">Data Lake Analytics 계정에서 방화벽 규칙 또는 방화벽 규칙 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06b9d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06b9d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06b9d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="06b9d-106">**AzureRmDataLakeAnalyticsFirewallRule** Cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙 또는 방화벽 규칙 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="06b9d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="06b9d-108">예제 1: 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="06b9d-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="06b9d-109">이 명령은 "ContosoAdlAcct" 계정의 "내 방화벽 규칙" 이라는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="06b9d-110">예제 2: 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="06b9d-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="06b9d-111">이 명령은 "ContosoAdlAcct" 계정에서 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="06b9d-112">변수</span><span class="sxs-lookup"><span data-stu-id="06b9d-112">PARAMETERS</span></span>

### <span data-ttu-id="06b9d-113">-계정</span><span class="sxs-lookup"><span data-stu-id="06b9d-113">-Account</span></span>
<span data-ttu-id="06b9d-114">방화벽 규칙을 가져오는 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="06b9d-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b9d-115">-DefaultProfile</span></span>
<span data-ttu-id="06b9d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06b9d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b9d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="06b9d-117">-Name</span></span>
<span data-ttu-id="06b9d-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b9d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b9d-119">-ResourceGroupName</span></span>
<span data-ttu-id="06b9d-120">계정을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b9d-121">CommonParameters</span></span>
<span data-ttu-id="06b9d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06b9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b9d-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b9d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b9d-124">입력</span><span class="sxs-lookup"><span data-stu-id="06b9d-124">INPUTS</span></span>

### <span data-ttu-id="06b9d-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06b9d-125">System.String</span></span>

## <span data-ttu-id="06b9d-126">출력</span><span class="sxs-lookup"><span data-stu-id="06b9d-126">OUTPUTS</span></span>

### <span data-ttu-id="06b9d-127">DataLakeAnalytics. DataLakeAnalyticsFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="06b9d-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="06b9d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="06b9d-128">NOTES</span></span>

## <span data-ttu-id="06b9d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06b9d-129">RELATED LINKS</span></span>