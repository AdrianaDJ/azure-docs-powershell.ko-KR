---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3f7ee823441910e1e5e79da3901d4114f04fdd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308741"
---
# <span data-ttu-id="9e45c-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="9e45c-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="9e45c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e45c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e45c-103">관리 되는 응용 프로그램 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e45c-103">Updates managed application definition</span></span>

## <span data-ttu-id="9e45c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e45c-104">SYNTAX</span></span>

### <span data-ttu-id="9e45c-105">SetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="9e45c-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e45c-106">SetById</span><span class="sxs-lookup"><span data-stu-id="9e45c-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e45c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9e45c-107">DESCRIPTION</span></span>
<span data-ttu-id="9e45c-108">**AzManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="9e45c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9e45c-109">EXAMPLES</span></span>

### <span data-ttu-id="9e45c-110">예제 1: 관리 되는 응용 프로그램 정의 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e45c-110">Example 1: Update managed application definition description</span></span>
```powershell
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="9e45c-111">이 명령은 관리 되는 응용 프로그램 정의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-111">This command updates the managed application definition description</span></span>

### <span data-ttu-id="9e45c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e45c-112">Example 2</span></span>

<span data-ttu-id="9e45c-113">관리 되는 응용 프로그램 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-113">Updates managed application definition.</span></span> <span data-ttu-id="9e45c-114">생성</span><span class="sxs-lookup"><span data-stu-id="9e45c-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzManagedApplicationDefinition -Id '/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef' -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip
```

## <span data-ttu-id="9e45c-115">변수</span><span class="sxs-lookup"><span data-stu-id="9e45c-115">PARAMETERS</span></span>

### <span data-ttu-id="9e45c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e45c-116">-ApiVersion</span></span>
<span data-ttu-id="9e45c-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9e45c-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9e45c-119">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="9e45c-119">-Authorization</span></span>
<span data-ttu-id="9e45c-120">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-120">The managed application definition authorization.</span></span>
<span data-ttu-id="9e45c-121">다음과 같은 형식으로 쉼표로 구분 된 인증 쌍 \<principalId\>\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="9e45c-121">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e45c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e45c-122">-DefaultProfile</span></span>
<span data-ttu-id="9e45c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e45c-124">-설명</span><span class="sxs-lookup"><span data-stu-id="9e45c-124">-Description</span></span>
<span data-ttu-id="9e45c-125">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-125">The managed application definition description.</span></span>

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

### <span data-ttu-id="9e45c-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9e45c-126">-DisplayName</span></span>
<span data-ttu-id="9e45c-127">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-127">The managed application definition display name.</span></span>

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

### <span data-ttu-id="9e45c-128">-Id</span><span class="sxs-lookup"><span data-stu-id="9e45c-128">-Id</span></span>
<span data-ttu-id="9e45c-129">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-129">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="9e45c-130">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e45c-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e45c-131">-이름</span><span class="sxs-lookup"><span data-stu-id="9e45c-131">-Name</span></span>
<span data-ttu-id="9e45c-132">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-132">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e45c-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="9e45c-133">-PackageFileUri</span></span>
<span data-ttu-id="9e45c-134">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="9e45c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="9e45c-135">-Pre</span></span>
<span data-ttu-id="9e45c-136">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9e45c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e45c-137">-ResourceGroupName</span></span>
<span data-ttu-id="9e45c-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e45c-139">태그</span><span class="sxs-lookup"><span data-stu-id="9e45c-139">-Tag</span></span>
<span data-ttu-id="9e45c-140">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e45c-141">-확인</span><span class="sxs-lookup"><span data-stu-id="9e45c-141">-Confirm</span></span>
<span data-ttu-id="9e45c-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e45c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e45c-143">-WhatIf</span></span>
<span data-ttu-id="9e45c-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e45c-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e45c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e45c-146">CommonParameters</span></span>
<span data-ttu-id="9e45c-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e45c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e45c-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e45c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e45c-149">입력</span><span class="sxs-lookup"><span data-stu-id="9e45c-149">INPUTS</span></span>

### <span data-ttu-id="9e45c-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e45c-150">System.String</span></span>

### <span data-ttu-id="9e45c-151">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="9e45c-151">System.String[]</span></span>

### <span data-ttu-id="9e45c-152">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="9e45c-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e45c-153">출력</span><span class="sxs-lookup"><span data-stu-id="9e45c-153">OUTPUTS</span></span>

### <span data-ttu-id="9e45c-154">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="9e45c-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9e45c-155">상속자</span><span class="sxs-lookup"><span data-stu-id="9e45c-155">NOTES</span></span>

## <span data-ttu-id="9e45c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e45c-156">RELATED LINKS</span></span>