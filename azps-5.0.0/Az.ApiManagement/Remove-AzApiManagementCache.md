---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309730"
---
# <span data-ttu-id="52940-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="52940-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="52940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52940-102">SYNOPSIS</span></span>
<span data-ttu-id="52940-103">캐시 엔터티를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52940-103">Removes the cache entity.</span></span>

## <span data-ttu-id="52940-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52940-104">SYNTAX</span></span>

### <span data-ttu-id="52940-105">ContextParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="52940-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52940-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52940-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52940-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52940-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52940-108">설명은</span><span class="sxs-lookup"><span data-stu-id="52940-108">DESCRIPTION</span></span>
<span data-ttu-id="52940-109">Cmdlet **AzApiManagementCache** 는 캐시 엔터티를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52940-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="52940-110">예제의</span><span class="sxs-lookup"><span data-stu-id="52940-110">EXAMPLES</span></span>

### <span data-ttu-id="52940-111">예제 1: 캐시 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="52940-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="52940-112">이 cmdlet은 `centralus` Api Management 서비스에서 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52940-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="52940-113">변수</span><span class="sxs-lookup"><span data-stu-id="52940-113">PARAMETERS</span></span>

### <span data-ttu-id="52940-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="52940-114">-CacheId</span></span>
<span data-ttu-id="52940-115">기존 cacheId의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="52940-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52940-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="52940-117">-Context</span></span>
<span data-ttu-id="52940-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="52940-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52940-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52940-120">-DefaultProfile</span></span>
<span data-ttu-id="52940-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52940-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52940-122">-InputObject</span></span>
<span data-ttu-id="52940-123">PsApiManagementCache의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="52940-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52940-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52940-125">-PassThru</span></span>
<span data-ttu-id="52940-126">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="52940-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="52940-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-127">This parameter is optional.</span></span>
<span data-ttu-id="52940-128">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-128">Default value is false.</span></span>

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

### <span data-ttu-id="52940-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52940-129">-ResourceId</span></span>
<span data-ttu-id="52940-130">캐시의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="52940-131">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="52940-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52940-132">-확인</span><span class="sxs-lookup"><span data-stu-id="52940-132">-Confirm</span></span>
<span data-ttu-id="52940-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52940-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52940-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52940-134">-WhatIf</span></span>
<span data-ttu-id="52940-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52940-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52940-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52940-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52940-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52940-137">CommonParameters</span></span>
<span data-ttu-id="52940-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52940-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52940-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52940-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52940-140">입력</span><span class="sxs-lookup"><span data-stu-id="52940-140">INPUTS</span></span>

### <span data-ttu-id="52940-141">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52940-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52940-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52940-142">System.String</span></span>

### <span data-ttu-id="52940-143">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="52940-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52940-144">출력</span><span class="sxs-lookup"><span data-stu-id="52940-144">OUTPUTS</span></span>

### <span data-ttu-id="52940-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="52940-145">System.Boolean</span></span>

## <span data-ttu-id="52940-146">상속자</span><span class="sxs-lookup"><span data-stu-id="52940-146">NOTES</span></span>

## <span data-ttu-id="52940-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52940-147">RELATED LINKS</span></span>

[<span data-ttu-id="52940-148">새로운 AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="52940-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="52940-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="52940-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="52940-150">업데이트-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="52940-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)