---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: c1e4c3f748df4808fe570e95150450d3b3987d00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536015"
---
# <span data-ttu-id="2ccd3-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2ccd3-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="2ccd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ccd3-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccd3-103">지정 된 Data Lake Store 계정에 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ccd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ccd3-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ccd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ccd3-105">DESCRIPTION</span></span>
<span data-ttu-id="2ccd3-106">**추가-AzureRmDataLakeStoreFirewallRule** cmdlet은 지정 된 Data Lake store 계정에 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="2ccd3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ccd3-107">EXAMPLES</span></span>

### <span data-ttu-id="2ccd3-108">예제 1: Data Lake Store 계정에 새 방화벽 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="2ccd3-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="2ccd3-109">이렇게 하면 "ContosoADL" 계정에 "MyRule" 이라는 새 방화벽 규칙이 만들어집니다. IP 범위는 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="2ccd3-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="2ccd3-110">변수</span><span class="sxs-lookup"><span data-stu-id="2ccd3-110">PARAMETERS</span></span>

### <span data-ttu-id="2ccd3-111">-계정</span><span class="sxs-lookup"><span data-stu-id="2ccd3-111">-Account</span></span>
<span data-ttu-id="2ccd3-112">방화벽 규칙을 추가할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="2ccd3-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccd3-113">-DefaultProfile</span></span>
<span data-ttu-id="2ccd3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2ccd3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ccd3-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ccd3-115">-EndIpAddress</span></span>
<span data-ttu-id="2ccd3-116">방화벽 규칙에 대 한 유효한 ip 범위의 끝</span><span class="sxs-lookup"><span data-stu-id="2ccd3-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd3-117">-이름</span><span class="sxs-lookup"><span data-stu-id="2ccd3-117">-Name</span></span>
<span data-ttu-id="2ccd3-118">추가할 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="2ccd3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ccd3-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ccd3-120">방화벽 규칙을 추가할 계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd3-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ccd3-121">-StartIpAddress</span></span>
<span data-ttu-id="2ccd3-122">방화벽 규칙에 대 한 유효한 ip 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="2ccd3-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd3-123">-확인</span><span class="sxs-lookup"><span data-stu-id="2ccd3-123">-Confirm</span></span>
<span data-ttu-id="2ccd3-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ccd3-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ccd3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccd3-126">CommonParameters</span></span>
<span data-ttu-id="2ccd3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccd3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccd3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccd3-129">입력</span><span class="sxs-lookup"><span data-stu-id="2ccd3-129">INPUTS</span></span>

### <span data-ttu-id="2ccd3-130">않아야</span><span class="sxs-lookup"><span data-stu-id="2ccd3-130">None</span></span>
<span data-ttu-id="2ccd3-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ccd3-132">출력</span><span class="sxs-lookup"><span data-stu-id="2ccd3-132">OUTPUTS</span></span>

### <span data-ttu-id="2ccd3-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2ccd3-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="2ccd3-134">추가 된 방화벽 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="2ccd3-134">The firewall rule that was added.</span></span>

## <span data-ttu-id="2ccd3-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2ccd3-135">NOTES</span></span>

## <span data-ttu-id="2ccd3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ccd3-136">RELATED LINKS</span></span>
