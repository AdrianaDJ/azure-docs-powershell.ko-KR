---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711509"
---
# Get-AzureRmRecoveryServicesAsrVaultContext

## SYNOPSIS
복구 서비스 자격 증명 모음에 대 한 ASR vault 설정 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrVaultContext** Cmdlet은 복구 서비스 자격 증명 모음과 관련 된 ASR vault 설정 정보를 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

현재 활성 (PowerShell 세션) 복구 서비스 자격 증명 모음에 대 한 ASR vault 설정을 가져옵니다.

## 변수

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### SiteRecovery. ASRVaultSettings에 대 한 서비스

## 상속자

## 관련 링크
