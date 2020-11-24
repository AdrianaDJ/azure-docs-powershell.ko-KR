---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309589"
---
# <span data-ttu-id="ef684-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="ef684-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="ef684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef684-102">SYNOPSIS</span></span>
<span data-ttu-id="ef684-103">방화벽 조건에 대 한 일치 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="ef684-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef684-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef684-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef684-105">DESCRIPTION</span></span>
<span data-ttu-id="ef684-106">**AzApplicationGatewayFirewallMatchVariable** 는 방화벽 조건에 대 한 일치 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="ef684-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef684-107">EXAMPLES</span></span>

### <span data-ttu-id="ef684-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef684-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="ef684-109">명령에서 요청 헤더의 이름과 선택기의 내용 길이 필드가 포함 된 새 match 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="ef684-110">새 match 변수는 $variable에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="ef684-111">변수</span><span class="sxs-lookup"><span data-stu-id="ef684-111">PARAMETERS</span></span>

### <span data-ttu-id="ef684-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef684-112">-DefaultProfile</span></span>
<span data-ttu-id="ef684-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef684-114">-선택기</span><span class="sxs-lookup"><span data-stu-id="ef684-114">-Selector</span></span>
<span data-ttu-id="ef684-115">MatchVariable 컬렉션의 필드에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef684-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="ef684-116">-VariableName</span></span>
<span data-ttu-id="ef684-117">Match 변수</span><span class="sxs-lookup"><span data-stu-id="ef684-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef684-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef684-118">CommonParameters</span></span>
<span data-ttu-id="ef684-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef684-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef684-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef684-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef684-121">입력</span><span class="sxs-lookup"><span data-stu-id="ef684-121">INPUTS</span></span>

### <span data-ttu-id="ef684-122">않아야</span><span class="sxs-lookup"><span data-stu-id="ef684-122">None</span></span>

## <span data-ttu-id="ef684-123">출력</span><span class="sxs-lookup"><span data-stu-id="ef684-123">OUTPUTS</span></span>

### <span data-ttu-id="ef684-124">PSApplicationGatewayFirewallMatchVariable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ef684-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="ef684-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ef684-125">NOTES</span></span>

## <span data-ttu-id="ef684-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef684-126">RELATED LINKS</span></span>