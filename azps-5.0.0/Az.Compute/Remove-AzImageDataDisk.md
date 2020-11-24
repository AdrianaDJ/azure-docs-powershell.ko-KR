---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308447"
---
# <span data-ttu-id="a2948-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="a2948-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="a2948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2948-102">SYNOPSIS</span></span>
<span data-ttu-id="a2948-103">Image 개체에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="a2948-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2948-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2948-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2948-105">DESCRIPTION</span></span>
<span data-ttu-id="a2948-106">**AzImageDataDisk** cmdlet은 image 개체에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="a2948-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2948-107">EXAMPLES</span></span>

### <span data-ttu-id="a2948-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2948-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="a2948-109">이 명령은 리소스 그룹 ' ResourceGroup01 '의 기존 이미지 ' Image01 '에서 논리 단위 번호 1의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a2948-110">변수</span><span class="sxs-lookup"><span data-stu-id="a2948-110">PARAMETERS</span></span>

### <span data-ttu-id="a2948-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2948-111">-DefaultProfile</span></span>
<span data-ttu-id="a2948-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2948-113">-이미지</span><span class="sxs-lookup"><span data-stu-id="a2948-113">-Image</span></span>
<span data-ttu-id="a2948-114">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2948-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="a2948-115">-Lun</span></span>
<span data-ttu-id="a2948-116">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2948-117">-확인</span><span class="sxs-lookup"><span data-stu-id="a2948-117">-Confirm</span></span>
<span data-ttu-id="a2948-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2948-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2948-119">-WhatIf</span></span>
<span data-ttu-id="a2948-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2948-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2948-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2948-122">CommonParameters</span></span>
<span data-ttu-id="a2948-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2948-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2948-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2948-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2948-125">입력</span><span class="sxs-lookup"><span data-stu-id="a2948-125">INPUTS</span></span>

### <span data-ttu-id="a2948-126">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="a2948-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="a2948-127">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="a2948-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a2948-128">출력</span><span class="sxs-lookup"><span data-stu-id="a2948-128">OUTPUTS</span></span>

### <span data-ttu-id="a2948-129">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="a2948-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a2948-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a2948-130">NOTES</span></span>

## <span data-ttu-id="a2948-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2948-131">RELATED LINKS</span></span>