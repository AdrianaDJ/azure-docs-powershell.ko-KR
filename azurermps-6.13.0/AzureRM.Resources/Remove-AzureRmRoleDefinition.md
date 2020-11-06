---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 6669cdfad83c8e5f4299abe0d1297f7e0659a42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535644"
---
# <span data-ttu-id="0935e-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0935e-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="0935e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0935e-102">SYNOPSIS</span></span>
<span data-ttu-id="0935e-103">Azure RBAC에서 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="0935e-104">삭제할 역할은 역할의 Id 속성을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="0935e-105">사용자 지정 역할에 대 한 기존 역할 할당이 있으면 Delete가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0935e-106">구문과</span><span class="sxs-lookup"><span data-stu-id="0935e-106">SYNTAX</span></span>

### <span data-ttu-id="0935e-107">RoleDefinitionIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0935e-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0935e-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0935e-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0935e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0935e-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0935e-110">설명은</span><span class="sxs-lookup"><span data-stu-id="0935e-110">DESCRIPTION</span></span>
<span data-ttu-id="0935e-111">Remove-AzureRmRoleDefinition cmdlet은 Azure Role-Based 액세스 제어에서 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="0935e-112">기존 사용자 지정 역할의 Id 매개 변수를 제공 하 여 해당 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="0935e-113">기본적으로 Remove-AzureRmRoleDefinition 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="0935e-114">프롬프트를 표시 하지 않으려면 Force 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="0935e-115">사용자 지정 역할에 대해 삭제 될 기존 역할 할당이 있는 경우 삭제는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="0935e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="0935e-116">EXAMPLES</span></span>

### <span data-ttu-id="0935e-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="0935e-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="0935e-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="0935e-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="0935e-119">변수</span><span class="sxs-lookup"><span data-stu-id="0935e-119">PARAMETERS</span></span>

### <span data-ttu-id="0935e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0935e-120">-DefaultProfile</span></span>
<span data-ttu-id="0935e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0935e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0935e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0935e-122">-Force</span></span>
<span data-ttu-id="0935e-123">설정 하는 경우 사용자 지정 역할을 삭제 하기 전에 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="0935e-124">-Id</span><span class="sxs-lookup"><span data-stu-id="0935e-124">-Id</span></span>
<span data-ttu-id="0935e-125">삭제할 역할 정의의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0935e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0935e-126">-InputObject</span></span>
<span data-ttu-id="0935e-127">제거할 역할 정의를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0935e-128">-이름</span><span class="sxs-lookup"><span data-stu-id="0935e-128">-Name</span></span>
<span data-ttu-id="0935e-129">삭제할 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0935e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0935e-130">-PassThru</span></span>
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

### <span data-ttu-id="0935e-131">-범위</span><span class="sxs-lookup"><span data-stu-id="0935e-131">-Scope</span></span>
<span data-ttu-id="0935e-132">역할 정의 범위</span><span class="sxs-lookup"><span data-stu-id="0935e-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0935e-133">-확인</span><span class="sxs-lookup"><span data-stu-id="0935e-133">-Confirm</span></span>
<span data-ttu-id="0935e-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0935e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0935e-135">-WhatIf</span></span>
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

### <span data-ttu-id="0935e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0935e-136">CommonParameters</span></span>
<span data-ttu-id="0935e-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0935e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0935e-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0935e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0935e-139">입력</span><span class="sxs-lookup"><span data-stu-id="0935e-139">INPUTS</span></span>

### <span data-ttu-id="0935e-140">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="0935e-140">System.Guid</span></span>

### <span data-ttu-id="0935e-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0935e-141">System.String</span></span>

### <span data-ttu-id="0935e-142">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="0935e-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="0935e-143">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0935e-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0935e-144">출력</span><span class="sxs-lookup"><span data-stu-id="0935e-144">OUTPUTS</span></span>

### <span data-ttu-id="0935e-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0935e-145">System.Boolean</span></span>

## <span data-ttu-id="0935e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="0935e-146">NOTES</span></span>
<span data-ttu-id="0935e-147">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="0935e-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0935e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0935e-148">RELATED LINKS</span></span>

[<span data-ttu-id="0935e-149">새로운 AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0935e-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="0935e-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0935e-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="0935e-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0935e-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)
