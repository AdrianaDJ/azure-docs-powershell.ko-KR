---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523183"
---
# Get-AzureRmDeploymentManagerStep

## SYNOPSIS
배포 단계를 가져옵니다.

## 구문과

### 대화형 (기본값)
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 리소스
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureRmDeploymentManagerStep** cmdlet은 단계를 가져오고 해당 단계를 나타내는 개체를 반환 합니다.
해당 이름 및 리소스 그룹 이름으로 단계를 지정 합니다. 또는 Step 개체 또는 ResourceId를 제공할 수 있습니다.

이 개체를 로컬로 수정한 다음 Set-AzureRmDeploymentManagerStep cmdlet을 사용 하 여 아티팩트 원본에 변경 내용을 적용할 수 있습니다.

## 예제의

### 예제 1: 단계 가져오기
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 가져옵니다.

### 예제 2: 리소스 식별자를 사용 하 여 단계 가져오기
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 가져옵니다.

### 예제 3: New-AzureRmDeploymentManagerStep에서 반환 된 개체를 사용 하 여 단계 가져오기
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 이 명령은 name 및 ResourceGroup이 $stepObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 단계를 가져옵니다.


## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
단계의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -단계
단계 리소스 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.
자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### PSStepResource-. m i 매니저.

## 출력

### PSStepResource-. m i 매니저.

## 상속자

## 관련 링크
