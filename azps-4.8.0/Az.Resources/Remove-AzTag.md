---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 05ee8609c7ee8bccd435e6e861f67829b9988d74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204401"
---
# Remove-AzTag

## SYNOPSIS
미리 정의 된 Azure 태그 또는 값을 삭제 합니다. | 리소스나 구독에 대 한 전체 태그 집합을 삭제 합니다.

## 구문과

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## 설명은

**RemovePredefinedTagSet** : **Remove-AzTag** cmdlet은 구독에서 미리 정의 된 Azure 태그 및 값을 삭제 합니다.
미리 정의 된 태그에서 특정 값을 삭제 하려면 *Value* 매개 변수를 사용 합니다.
기본적으로 **-AzTag** 에서는 지정 된 태그와 모든 값을 삭제 합니다. 현재 리소스나 리소스 그룹에 적용 된 태그나 값은 삭제할 수 없습니다.
**Remove-AzTag** 를 사용 하기 전에 Set-AzResourceGroup Cmdlet의 *tag* 매개 변수를 사용 하 여 리소스 또는 리소스 그룹의 태그를 삭제 합니다.
**-AzTag를 제거** 하는 azure 태그 모듈은 미리 정의 된 azure 태그를 관리 하는 데 도움이 될 수 있습니다.
Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.
한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.

**RemoveByResourceIdParameterSet** : **ResourceId** 가 있는 **Remove-AzTag** cmdlet은 리소스나 구독에 대 한 전체 태그 집합을 삭제 합니다.

## 예제의

### 예제 1: 미리 정의 된 태그 삭제
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

이 명령은 부서별 및 모든 값 이라는 미리 정의 된 태그를 삭제 합니다.
해당 태그가 리소스나 리소스 그룹에 적용 되 면 명령이 실패 합니다.

### 예제 2: 미리 정의 된 태그에서 값 삭제
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

이 명령은 미리 정의 된 부서 태그에서 HumanResources 값을 삭제 합니다.
태그는 삭제 되지 않습니다.
값이 리소스나 리소스 그룹에 적용 되 면 명령이 실패 합니다.

### 예제 3: 구독에 대 한 전체 태그 집합 삭제

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

이 명령은 {subId}를 사용 하 여 구독에 대 한 전체 태그 집합을 삭제 합니다. "-PassThru"를 전달 하지 않으면 삭제 된 개체는 반환 되지 않습니다.

### 예제 4: 리소스의 전체 태그 집합 삭제

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

이 명령은 {resourceId}를 사용 하 여 리소스의 전체 태그 집합을 삭제 합니다. "-PassThru"를 전달할 때 삭제 된 oject를 반환 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
제거할 미리 정의 된 태그의 이름을 지정 합니다.
기본적으로 **AzTag 제거-** 지정 된 태그와 모든 값을 제거 합니다.
선택한 값만 삭제 하 고 태그는 삭제 하지 않으려면 *Value* 매개 변수를 사용 합니다.

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -값
미리 정의 된 태그에서 지정 된 값을 삭제 하지만 태그를 삭제 하지는 않습니다.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
태그가 지정 된 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정 될 수 있습니다.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
삭제 된 태그 또는 삭제 된 값이 있는 결과 태그를 나타내는 개체를 반환 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver []

### System.webserver 매개 변수

## 출력

### PSTag |을 (를) 보세요. PSTagResource에 대 한.

## 상속자

## 관련 링크

[Get-AzTag](./Get-AzTag.md)

[새로운 AzTag](./New-AzTag.md)

[업데이트-AzTag](./Update-AzTag.md)
