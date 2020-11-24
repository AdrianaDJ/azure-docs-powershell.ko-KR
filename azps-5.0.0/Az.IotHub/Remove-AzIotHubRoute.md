---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304691"
---
# <span data-ttu-id="f8d67-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="f8d67-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="f8d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d67-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d67-103">IoT Hub에서 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="f8d67-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="f8d67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8d67-104">SYNTAX</span></span>

### <span data-ttu-id="f8d67-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8d67-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d67-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8d67-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d67-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8d67-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d67-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f8d67-108">DESCRIPTION</span></span>
<span data-ttu-id="f8d67-109">끝점에 대 한 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="f8d67-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="f8d67-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f8d67-110">EXAMPLES</span></span>

### <span data-ttu-id="f8d67-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8d67-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="f8d67-112">"Myiothub" IoT Hub에서 "R1" 경로를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="f8d67-113">변수</span><span class="sxs-lookup"><span data-stu-id="f8d67-113">PARAMETERS</span></span>

### <span data-ttu-id="f8d67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d67-114">-DefaultProfile</span></span>
<span data-ttu-id="f8d67-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8d67-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8d67-116">-InputObject</span></span>
<span data-ttu-id="f8d67-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="f8d67-117">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d67-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f8d67-118">-Name</span></span>
<span data-ttu-id="f8d67-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="f8d67-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d67-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8d67-120">-PassThru</span></span>
<span data-ttu-id="f8d67-121">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-121">Allows to return the boolean object.</span></span> <span data-ttu-id="f8d67-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8d67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d67-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8d67-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-124">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d67-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d67-125">-ResourceId</span></span>
<span data-ttu-id="f8d67-126">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="f8d67-126">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d67-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="f8d67-127">-RouteName</span></span>
<span data-ttu-id="f8d67-128">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="f8d67-128">Name of the Route</span></span>

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

### <span data-ttu-id="f8d67-129">-확인</span><span class="sxs-lookup"><span data-stu-id="f8d67-129">-Confirm</span></span>
<span data-ttu-id="f8d67-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d67-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d67-131">-WhatIf</span></span>
<span data-ttu-id="f8d67-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d67-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d67-134">CommonParameters</span></span>
<span data-ttu-id="f8d67-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8d67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d67-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d67-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d67-137">입력</span><span class="sxs-lookup"><span data-stu-id="f8d67-137">INPUTS</span></span>

### <span data-ttu-id="f8d67-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="f8d67-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f8d67-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f8d67-139">System.String</span></span>

## <span data-ttu-id="f8d67-140">출력</span><span class="sxs-lookup"><span data-stu-id="f8d67-140">OUTPUTS</span></span>

### <span data-ttu-id="f8d67-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f8d67-141">System.Boolean</span></span>

## <span data-ttu-id="f8d67-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f8d67-142">NOTES</span></span>

## <span data-ttu-id="f8d67-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8d67-143">RELATED LINKS</span></span>