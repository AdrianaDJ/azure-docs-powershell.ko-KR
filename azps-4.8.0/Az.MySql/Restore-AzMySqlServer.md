---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048978"
---
# Restore-AzMySqlServer

## SYNOPSIS
기존 백업에서 서버 복원

## 구문과

### GeoRestore (기본값)
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### PointInTimeRestore
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## 설명은
기존 백업에서 서버 복원

## 예제의

### 예제 1: GeoReplica Restore를 사용 하 여 MySql 서버 복원
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

이 cmdlet은 GeoReplica Restore를 사용 하 여 MySql 서버를 복원 합니다.

### 예제 2: PointInTime Restore를 사용 하 여 MySql 서버 복원
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

이러한 cmdlet은 PointInTime Restore를 사용 하 여 MySql 서버를 복원 합니다.

## 변수

### -AsJob
명령을 작업으로 실행 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
복원할 원본 서버 개체입니다.
생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -위치
리소스가 있는 위치입니다.

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

### -이름
서버의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
비동기적으로 명령을 실행 합니다.

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

### -ResourceGroupName
리소스가 포함 된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorePointInTime
리소스가 있는 위치입니다.

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.

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
Azure 구독을 식별 하는 구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseGeoRestore
지역 모드를 사용 하 여 복원

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePointInTimeRestore
PointInTime 모드를 사용 하 여 복원

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Api20171201 (Microsoft. i m/. i m/. i m/. 서버)

## 출력

### Api20171201 (Microsoft. i m/. i m/. i m/. 서버)

## 상속자

별칭과

복합 매개 변수 속성

아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.


INPUTOBJECT <IServer> : 복원할 원본 서버 개체입니다.
  - `Location <String>`: 리소스가 있는 위치입니다.
  - `[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터
    - `[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다. 서버를 만드는 경우에만 지정할 수 있습니다 (만들기에 필요 함).
  - `[EarliestRestoreDate <DateTime?>]`: 초기 복원 시점 생성 시간 (ISO8601 형식)
  - `[FullyQualifiedDomainName <String>]`: 서버의 정규화 된 도메인 이름입니다.
  - `[IdentityType <IdentityType?>]`: Id 형식입니다. 해당 리소스에 대 한 Azure Active Directory 보안 주체를 자동으로 만들고 할당 하려면이를 ' SystemAssigned '로 설정 합니다.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버에서 인프라 암호화를 사용 하는지 여부를 나타내는 상태입니다.
  - `[MasterServerId <String>]`: 복제본 서버의 마스터 서버 id입니다.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 대해 최소 Tls 버전을 적용 합니다.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`:이 서버에 공용 네트워크 액세스가 허용 되는지 여부 값은 선택 사항 이지만, 전달 되는 경우에는 ' Enabled ' 또는 ' Disabled ' 여야 합니다.
  - `[ReplicaCapacity <Int32?>]`: 마스터 서버에 포함할 수 있는 최대 복제 데이터베이스 수입니다.
  - `[ReplicationRole <String>]`: 서버의 복제 역할입니다.
  - `[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 스케일 업/out 용량입니다.
  - `[SkuFamily <String>]`: 하드웨어의 패밀리입니다.
  - `[SkuName <String>]`: Sku의 이름 (일반적으로 계층 + 패밀리 + 코어) (예: B_Gen4_1 GP_Gen5_8)입니다.
  - `[SkuSize <String>]`: 리소스에 따라 적절 하 게 해석 되는 크기 코드입니다.
  - `[SkuTier <SkuTier?>]`: 특정 SKU (예: 기본)의 계층입니다.
  - `[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용 여부를 설정 합니다.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대 한 백업 보존 일입니다.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지리적 중복을 사용 하거나 사용할 수 없습니다.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용 합니다.
  - `[StorageProfileStorageMb <Int32?>]`: 서버에 허용 된 최대 저장소.
  - `[UserVisibleState <ServerState?>]`: 사용자에 게 표시 되는 서버의 상태입니다.
  - `[Version <ServerVersion?>]`: 서버 버전.

## 관련 링크

