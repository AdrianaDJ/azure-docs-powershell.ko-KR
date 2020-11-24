---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304163"
---
# <span data-ttu-id="22aa4-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="22aa4-101">Update-AzImage</span></span>

## <span data-ttu-id="22aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="22aa4-103">이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-103">Updates an image.</span></span>

## <span data-ttu-id="22aa4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22aa4-104">SYNTAX</span></span>

### <span data-ttu-id="22aa4-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="22aa4-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22aa4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="22aa4-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22aa4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="22aa4-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22aa4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="22aa4-108">DESCRIPTION</span></span>
<span data-ttu-id="22aa4-109">**업데이트 AzImage** cmdlet은 이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="22aa4-110">현재 태그만 업데이트 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="22aa4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="22aa4-111">EXAMPLES</span></span>

### <span data-ttu-id="22aa4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="22aa4-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="22aa4-113">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 기존 이미지 ' Image01 '의 태그 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="22aa4-114">변수</span><span class="sxs-lookup"><span data-stu-id="22aa4-114">PARAMETERS</span></span>

### <span data-ttu-id="22aa4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22aa4-115">-AsJob</span></span>
<span data-ttu-id="22aa4-116">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-116">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22aa4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22aa4-117">-DefaultProfile</span></span>
<span data-ttu-id="22aa4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22aa4-119">-이미지</span><span class="sxs-lookup"><span data-stu-id="22aa4-119">-Image</span></span>
<span data-ttu-id="22aa4-120">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22aa4-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="22aa4-121">-ImageName</span></span>
<span data-ttu-id="22aa4-122">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22aa4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22aa4-123">-ResourceGroupName</span></span>
<span data-ttu-id="22aa4-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22aa4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22aa4-125">-ResourceId</span></span>
<span data-ttu-id="22aa4-126">이미지의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="22aa4-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22aa4-127">태그</span><span class="sxs-lookup"><span data-stu-id="22aa4-127">-Tag</span></span>
<span data-ttu-id="22aa4-128">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="22aa4-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22aa4-129">-확인</span><span class="sxs-lookup"><span data-stu-id="22aa4-129">-Confirm</span></span>
<span data-ttu-id="22aa4-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22aa4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22aa4-131">-WhatIf</span></span>
<span data-ttu-id="22aa4-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22aa4-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22aa4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22aa4-134">CommonParameters</span></span>
<span data-ttu-id="22aa4-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22aa4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22aa4-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="22aa4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22aa4-137">입력</span><span class="sxs-lookup"><span data-stu-id="22aa4-137">INPUTS</span></span>

### <span data-ttu-id="22aa4-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22aa4-138">System.String</span></span>

### <span data-ttu-id="22aa4-139">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="22aa4-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="22aa4-140">출력</span><span class="sxs-lookup"><span data-stu-id="22aa4-140">OUTPUTS</span></span>

### <span data-ttu-id="22aa4-141">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="22aa4-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="22aa4-142">상속자</span><span class="sxs-lookup"><span data-stu-id="22aa4-142">NOTES</span></span>

## <span data-ttu-id="22aa4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22aa4-143">RELATED LINKS</span></span>