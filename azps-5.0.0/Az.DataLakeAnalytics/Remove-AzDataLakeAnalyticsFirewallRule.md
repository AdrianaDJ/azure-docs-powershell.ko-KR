---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305774"
---
# <span data-ttu-id="ae66e-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ae66e-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ae66e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae66e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae66e-103">Data Lake Analytics 계정에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ae66e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae66e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae66e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae66e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae66e-106">**AzDataLakeAnalyticsFirewallRule** Cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ae66e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae66e-107">EXAMPLES</span></span>

### <span data-ttu-id="ae66e-108">예제 1: 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="ae66e-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="ae66e-109">이 명령은 "ContosoAdlAcct" 계정의 "내 방화벽 규칙" 이라는 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="ae66e-110">변수</span><span class="sxs-lookup"><span data-stu-id="ae66e-110">PARAMETERS</span></span>

### <span data-ttu-id="ae66e-111">-계정</span><span class="sxs-lookup"><span data-stu-id="ae66e-111">-Account</span></span>
<span data-ttu-id="ae66e-112">방화벽 규칙을 제거할 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="ae66e-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="ae66e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae66e-113">-DefaultProfile</span></span>
<span data-ttu-id="ae66e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae66e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae66e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ae66e-115">-Name</span></span>
<span data-ttu-id="ae66e-116">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ae66e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae66e-117">-PassThru</span></span>
<span data-ttu-id="ae66e-118">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae66e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae66e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae66e-120">계정을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae66e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ae66e-121">-Confirm</span></span>
<span data-ttu-id="ae66e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae66e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae66e-123">-WhatIf</span></span>
<span data-ttu-id="ae66e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae66e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae66e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae66e-126">CommonParameters</span></span>
<span data-ttu-id="ae66e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae66e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae66e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae66e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae66e-129">입력</span><span class="sxs-lookup"><span data-stu-id="ae66e-129">INPUTS</span></span>

### <span data-ttu-id="ae66e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae66e-130">System.String</span></span>

### <span data-ttu-id="ae66e-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae66e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae66e-132">출력</span><span class="sxs-lookup"><span data-stu-id="ae66e-132">OUTPUTS</span></span>

### <span data-ttu-id="ae66e-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ae66e-133">System.Boolean</span></span>

## <span data-ttu-id="ae66e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ae66e-134">NOTES</span></span>

## <span data-ttu-id="ae66e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae66e-135">RELATED LINKS</span></span>