---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216034"
---
# Get-AzPolicyEvent

## SYNOPSIS
리소스가 만들어지거나 업데이트 될 때 생성 되는 정책 평가 이벤트를 가져옵니다.

## 구문과

### 구독 범위 (기본값)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
리소스가 만들어지거나 업데이트 될 때 생성 되는 정책 평가 이벤트를 가져옵니다. 정책 이벤트 레코드는 지정 된 시간 간격에 따라 다양 한 범위에서 쿼리할 수 있습니다 (기본적으로 마지막 날). 결과를 필터링 하 고 그룹화 하 고 그룹 집계를 계산할 수 있습니다.

## 예제의

### 예제 1: 현재 구독 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 2: 지정 된 구독 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

지정 된 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 3: 관리 그룹 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

지정 된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 4: 현재 구독의 리소스 그룹 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

지정 된 리소스 그룹 (현재 세션 컨텍스트의 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 5: 지정 된 구독의 리소스 그룹 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

지정 된 리소스 그룹 (지정 된 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 6: 리소스에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

지정 된 리소스의 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 7: 현재 구독에서 정책 집합 정의에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

현재 세션 컨텍스트의 구독에 있는 지정 된 정책 집합 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 8: 지정 된 구독에서 정책 집합 정의에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정 된 정책 집합 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 9: 현재 구독에서 정책 정의에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

현재 세션 컨텍스트의 구독에 있는 지정 된 정책 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 10: 지정 된 구독에서 정책 정의에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정 된 정책 정의 (지정 된 구독에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 11: 현재 구독에서 정책 할당에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정 된 정책 할당 (현재 세션 컨텍스트의 구독에 있음)에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예 12: 지정 된 구독에서 정책 할당에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정 된 정책 할당 (지정 된 구독에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 13: 현재 구독에서 지정 된 리소스 그룹의 정책 할당에 대 한 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정 된 정책 할당 (현재 세션 컨텍스트에서 구독에 있는 리소스 그룹에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 14: 현재 구독 범위에서 정책 이벤트 가져오기-OrderBy 사용, 상위 및 선택 쿼리 옵션
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다. 이 명령은 타임 스탬프 및 정책 할당 이름 속성을 기준으로 결과를 정렬 하 고 해당 순서로 나열 된 상위 5 개만 가져옵니다.
또한 각 레코드에 대 한 열의 하위 집합만 나열 하도록 선택 됩니다.

### 예제 15: From 및 To 쿼리 옵션을 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정 된 날짜 범위 내에서 생성 된 정책 이벤트 레코드를 가져옵니다.

### 예제 16: 필터 쿼리 옵션을 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.
이 명령은 정책 정의 작업 (거부 또는 감사 작업 포함) 및 리소스 위치 (e\ us 위치 제외)에 따라 필터링 하 여 반환 되는 결과를 제한 합니다.

### 예제 17: Apply를 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기 행 개수 집계 지정
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드의 수를 가져옵니다.
이 명령은 AdditionalProperties 속성 내에서 반환 되는 정책 이벤트 레코드의 수만 반환 합니다.

### 예 18: Apply를 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기 집계로 그룹화 지정
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다. 이 명령은 정책 정의 작업 (감사 및 거부 이벤트만 포함)을 기준으로 필터링 하 여 반환 되는 결과를 제한 합니다.
정책 할당, 정책 정의, 정책 정의 작업, 리소스 id를 기준으로 결과를 그룹화 하 고 AdditionalProperties 속성 내에서 반환 되는 각 그룹의 레코드 수를 계산 합니다.
결과를 개수 집계 별로 내림차순으로 정렬 하 고 해당 순서로 나열 된 상위 5 개만 가져옵니다.

### 예제 19: 현재 구독 범위에서 정책 이벤트 가져오기, 적용을 사용 하 여 집계 없이 그룹화 지정
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다. 이 명령은 정책 정의 작업 (감사 및 거부 이벤트만 포함)을 기준으로 필터링 하 여 반환 되는 결과를 제한 합니다.
리소스 id를 기준으로 결과를 그룹화 합니다. 이렇게 하면 하나 이상의 감사 또는 거부 정책에 대 한 정책 이벤트를 생성 한 구독 내의 모든 리소스 목록이 생성 됩니다.

### 예제 20: 적용을 통해 현재 구독 범위에서 정책 이벤트 가져오기 여러 그룹화 지정
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다. 이 명령은 정책 정의 작업 (거부 이벤트만 포함)을 기준으로 필터링 하 여 반환 되는 결과를 제한 합니다.
정책 할당, 정책 정의 및 리소스 id를 기준으로 결과를 먼저 그룹화 합니다. 그런 다음이 그룹화의 결과를 리소스 id를 제외한 동일한 속성으로 그룹화 하 고, AdditionalProperties 속성 내에서 반환 되는 이러한 각 그룹의 레코드 수를 계산 합니다.
결과를 개수 집계 별로 내림차순으로 정렬 하 고 해당 순서로 나열 된 상위 5 개만 가져옵니다.
이렇게 하면 최대 거부 리소스를 포함 하는 상위 5 개 거부 정책이 생성 됩니다.

## 변수

### -Apply
OData 표시법을 사용 하 여 집계에 대 한 식을 적용 합니다.

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

### -필터
OData 표시법을 사용 하 여 식을 필터링 합니다.

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

### -보낸 사람
쿼리 간격의 시작 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.
지정 하지 않으면 기본적으로 ' To ' 매개 변수 값은 1 일을 뺀 수입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
관리 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
OData 표시법을 사용 하는 정렬 식입니다.
선택적 ' desc ' (기본값) 또는 ' asc '가 있는 하나 이상의 쉼표로 구분 된 열 이름입니다.

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

### -PolicyAssignmentName
정책 할당 이름입니다.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
정책 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
정책 집합 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -선택
OData 표시법을 사용 하 여 식을 선택 합니다.
하나 이상의 쉼표로 구분 된 열 이름입니다.
각 레코드의 열을 요청한 값 으로만 제한 합니다.

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

### -SubscriptionId
구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
쿼리 간격의 종료 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.
지정 하지 않으면 기본적으로 요청 시간이 발생 합니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위쪽
반환할 레코드의 최대 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### Microsoft. Azure. PolicyInsights. * 정책 이벤트

## 상속자

## 관련 링크
