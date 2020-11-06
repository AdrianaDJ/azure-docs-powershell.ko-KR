---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2dbd515877e44023077d782080cff29d78a0e6fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536859"
---
# <span data-ttu-id="6bd5e-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6bd5e-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="6bd5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd5e-103">API 관리로 거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bd5e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd5e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6bd5e-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd5e-106">**AzureRmApiManagementLogger** Cmdlet은 Azure API Management **로 거** 를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="6bd5e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6bd5e-107">EXAMPLES</span></span>

### <span data-ttu-id="6bd5e-108">예제 1:로 거 제거</span><span class="sxs-lookup"><span data-stu-id="6bd5e-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="6bd5e-109">이 명령은 ID Logger123를 가진로 거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6bd5e-110">변수</span><span class="sxs-lookup"><span data-stu-id="6bd5e-110">PARAMETERS</span></span>

### <span data-ttu-id="6bd5e-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6bd5e-111">-Context</span></span>
<span data-ttu-id="6bd5e-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd5e-113">-DefaultProfile</span></span>
<span data-ttu-id="6bd5e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6bd5e-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="6bd5e-115">-LoggerId</span></span>
<span data-ttu-id="6bd5e-116">제거할로 거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-116">Specifies the ID of the logger to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd5e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bd5e-117">-PassThru</span></span>
<span data-ttu-id="6bd5e-118">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd5e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="6bd5e-119">-Confirm</span></span>
<span data-ttu-id="6bd5e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd5e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd5e-121">-WhatIf</span></span>
<span data-ttu-id="6bd5e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd5e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd5e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd5e-124">CommonParameters</span></span>
<span data-ttu-id="6bd5e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd5e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd5e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd5e-127">입력</span><span class="sxs-lookup"><span data-stu-id="6bd5e-127">INPUTS</span></span>

### <span data-ttu-id="6bd5e-128">않아야</span><span class="sxs-lookup"><span data-stu-id="6bd5e-128">None</span></span>
<span data-ttu-id="6bd5e-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bd5e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bd5e-130">출력</span><span class="sxs-lookup"><span data-stu-id="6bd5e-130">OUTPUTS</span></span>

### <span data-ttu-id="6bd5e-131">나타내는</span><span class="sxs-lookup"><span data-stu-id="6bd5e-131">Boolean</span></span>

## <span data-ttu-id="6bd5e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6bd5e-132">NOTES</span></span>

## <span data-ttu-id="6bd5e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bd5e-133">RELATED LINKS</span></span>

[<span data-ttu-id="6bd5e-134">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6bd5e-134">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6bd5e-135">새로운 AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6bd5e-135">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6bd5e-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6bd5e-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)

