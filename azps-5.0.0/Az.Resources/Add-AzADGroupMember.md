---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309918"
---
# <span data-ttu-id="23242-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="23242-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="23242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23242-102">SYNOPSIS</span></span>
<span data-ttu-id="23242-103">기존 광고 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="23242-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23242-104">SYNTAX</span></span>

### <span data-ttu-id="23242-105">MemberObjectIdWithGroupObjectId (기본값)</span><span class="sxs-lookup"><span data-stu-id="23242-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23242-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="23242-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23242-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="23242-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23242-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23242-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23242-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23242-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23242-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23242-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23242-111">설명은</span><span class="sxs-lookup"><span data-stu-id="23242-111">DESCRIPTION</span></span>
<span data-ttu-id="23242-112">기존 광고 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="23242-113">예제의</span><span class="sxs-lookup"><span data-stu-id="23242-113">EXAMPLES</span></span>

### <span data-ttu-id="23242-114">예제 1: 개체 id를 사용 하 여 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="23242-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="23242-115">개체 id가 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' 인 사용자를 개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="23242-116">예제 2: 파이핑을 사용 하 여 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="23242-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="23242-117">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져와이 그룹에 사용자를 추가 하도록 Add-AzADGroupMember cmdlet에 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="23242-118">예제 3: principal name을 기준으로 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="23242-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="23242-119">그룹에 사용자를 추가 하 고 그룹 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="23242-120">변수</span><span class="sxs-lookup"><span data-stu-id="23242-120">PARAMETERS</span></span>

### <span data-ttu-id="23242-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23242-121">-DefaultProfile</span></span>
<span data-ttu-id="23242-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23242-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23242-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="23242-123">-MemberObjectId</span></span>
<span data-ttu-id="23242-124">구성원의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="23242-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23242-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="23242-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="23242-126">그룹에 추가할 구성원의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="23242-126">The UPN of the member(s) to add to the group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23242-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23242-127">-PassThru</span></span>
<span data-ttu-id="23242-128">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="23242-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="23242-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="23242-130">구성원을 추가할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23242-130">The display name of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23242-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="23242-131">-TargetGroupObject</span></span>
<span data-ttu-id="23242-132">구성원을 추가할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="23242-132">The object representation of the group to add the member(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23242-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="23242-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="23242-134">구성원을 추가할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="23242-134">The object id of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23242-135">-확인</span><span class="sxs-lookup"><span data-stu-id="23242-135">-Confirm</span></span>
<span data-ttu-id="23242-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23242-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23242-137">-WhatIf</span></span>
<span data-ttu-id="23242-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23242-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23242-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23242-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23242-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23242-140">CommonParameters</span></span>
<span data-ttu-id="23242-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23242-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23242-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23242-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23242-143">입력</span><span class="sxs-lookup"><span data-stu-id="23242-143">INPUTS</span></span>

### <span data-ttu-id="23242-144">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="23242-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="23242-145">출력</span><span class="sxs-lookup"><span data-stu-id="23242-145">OUTPUTS</span></span>

### <span data-ttu-id="23242-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="23242-146">System.Boolean</span></span>

## <span data-ttu-id="23242-147">상속자</span><span class="sxs-lookup"><span data-stu-id="23242-147">NOTES</span></span>

## <span data-ttu-id="23242-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23242-148">RELATED LINKS</span></span>