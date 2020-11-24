---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310385"
---
# <span data-ttu-id="cea3f-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="cea3f-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="cea3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea3f-102">SYNOPSIS</span></span>
<span data-ttu-id="cea3f-103">지정 된 디스크 암호화 집합과 연결 된 리소스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="cea3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cea3f-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cea3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cea3f-105">DESCRIPTION</span></span>
<span data-ttu-id="cea3f-106">**AzDiskEncryptionSetAssociatedResource** cmdlet은 지정 된 디스크 암호화 집합과 연결 된 리소스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="cea3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cea3f-107">EXAMPLES</span></span>

### <span data-ttu-id="cea3f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cea3f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="cea3f-109">Cmdlet은 제공 된 디스크 암호화 집합과 연결 된 두 리소스 (' exampleDisk01 ' 및 ' exampleDisk02 ')를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="cea3f-110">변수</span><span class="sxs-lookup"><span data-stu-id="cea3f-110">PARAMETERS</span></span>

### <span data-ttu-id="cea3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea3f-111">-DefaultProfile</span></span>
<span data-ttu-id="cea3f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cea3f-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="cea3f-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="cea3f-114">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="cea3f-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cea3f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea3f-117">CommonParameters</span></span>
<span data-ttu-id="cea3f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea3f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea3f-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cea3f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea3f-120">입력</span><span class="sxs-lookup"><span data-stu-id="cea3f-120">INPUTS</span></span>

### <span data-ttu-id="cea3f-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cea3f-121">System.String</span></span>

## <span data-ttu-id="cea3f-122">출력</span><span class="sxs-lookup"><span data-stu-id="cea3f-122">OUTPUTS</span></span>

### <span data-ttu-id="cea3f-123">System. Uri []</span><span class="sxs-lookup"><span data-stu-id="cea3f-123">System.Uri[]</span></span>

## <span data-ttu-id="cea3f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="cea3f-124">NOTES</span></span>

## <span data-ttu-id="cea3f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cea3f-125">RELATED LINKS</span></span>