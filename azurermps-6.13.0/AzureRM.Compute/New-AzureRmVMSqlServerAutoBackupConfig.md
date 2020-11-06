---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: da85c91aea3c47c2b3ba0e9ff19938980dbc80d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534439"
---
# <span data-ttu-id="da608-101">New-AzureRmVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="da608-101">New-AzureRmVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="da608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da608-102">SYNOPSIS</span></span>
<span data-ttu-id="da608-103">SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da608-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da608-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da608-104">SYNTAX</span></span>

### <span data-ttu-id="da608-105">StorageUriSqlServerAutoBackup (기본값)</span><span class="sxs-lookup"><span data-stu-id="da608-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da608-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="da608-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da608-107">설명은</span><span class="sxs-lookup"><span data-stu-id="da608-107">DESCRIPTION</span></span>
<span data-ttu-id="da608-108">**AzureRmVMSqlServerAutoBackupConfig** CMDLET은 SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da608-108">The **New-AzureRmVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="da608-109">예제의</span><span class="sxs-lookup"><span data-stu-id="da608-109">EXAMPLES</span></span>

### <span data-ttu-id="da608-110">예제 1: 저장소 URI 및 계정 키를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="da608-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="da608-111">이 명령은 저장소 URI 및 계정 키를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da608-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="da608-112">자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da608-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="da608-113">명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="da608-114">Set-AzureRmVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da608-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="da608-115">예제 2: 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="da608-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="da608-116">첫 번째 명령은 저장소 컨텍스트를 만든 다음 $StorageContext 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="da608-117">자세한 내용은 새 AzureStorageContext를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da608-117">For more information, see New-AzureStorageContext.</span></span>
<span data-ttu-id="da608-118">두 번째 명령은 $StorageContext에서 저장소 컨텍스트를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da608-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="da608-119">자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da608-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="da608-120">예제 3: 암호화 및 암호를 사용 하 여 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="da608-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="da608-121">이 명령은 자동 백업 구성 개체를 만들고 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="da608-122">명령은 이전 예제에서 만든 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="da608-123">명령이 암호로 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-123">The command enables encryption with password.</span></span>
<span data-ttu-id="da608-124">암호가 이전에 $CertificatePassword 변수에 보안 문자열로 저장 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="da608-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="da608-125">보안 문자열을 만들려면 ConvertTo-SecureString cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="da608-126">변수</span><span class="sxs-lookup"><span data-stu-id="da608-126">PARAMETERS</span></span>

### <span data-ttu-id="da608-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="da608-127">-BackupScheduleType</span></span>
<span data-ttu-id="da608-128">백업 일정 유형, 수동 또는 자동</span><span class="sxs-lookup"><span data-stu-id="da608-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="da608-129">-BackupSystemDbs</span></span>
<span data-ttu-id="da608-130">시스템 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="da608-130">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="da608-131">-CertificatePassword</span></span>
<span data-ttu-id="da608-132">SQL Server 암호화 백업을 수행 하는 데 사용 되는 인증서를 암호화 하는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da608-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da608-133">-DefaultProfile</span></span>
<span data-ttu-id="da608-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da608-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da608-135">-사용</span><span class="sxs-lookup"><span data-stu-id="da608-135">-Enable</span></span>
<span data-ttu-id="da608-136">SQL Server 가상 컴퓨터에 대해 자동화 된 백업을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da608-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="da608-137">이 매개 변수를 지정 하면 자동 백업이 모든 현재 및 새 데이터베이스에 대 한 백업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="da608-138">이렇게 하면 관리 되는 백업 설정이 다음 일정을 따라 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da608-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="da608-139">-EnableEncryption</span></span>
<span data-ttu-id="da608-140">이 cmdlet이 암호화를 사용 하도록 설정 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da608-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="da608-141">-FullBackupFrequency</span></span>
<span data-ttu-id="da608-142">Sql Server 전체 백업 빈도 (매일 또는 매주)</span><span class="sxs-lookup"><span data-stu-id="da608-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-143">-Fullbackupstarth</span><span class="sxs-lookup"><span data-stu-id="da608-143">-FullBackupStartHour</span></span>
<span data-ttu-id="da608-144">Sql Server 전체 백업을 시작 해야 하는 날짜의 시간 (0-23)</span><span class="sxs-lookup"><span data-stu-id="da608-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="da608-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="da608-146">Sql Server 전체 백업 창 (시간)</span><span class="sxs-lookup"><span data-stu-id="da608-146">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="da608-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="da608-148">Sql Server 로그 백업 빈도 (1-60 분 마다 한 번)</span><span class="sxs-lookup"><span data-stu-id="da608-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da608-149">-ResourceGroupName</span></span>
<span data-ttu-id="da608-150">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="da608-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="da608-152">백업을 유지할 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="da608-153">-StorageContext</span></span>
<span data-ttu-id="da608-154">백업을 저장 하는 데 사용 되는 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="da608-155">**Azurestoragecontext** 개체를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="da608-156">기본값은 SQL Server 가상 컴퓨터와 연결 된 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="da608-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="da608-157">-StorageKey</span></span>
<span data-ttu-id="da608-158">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="da608-159">-StorageUri</span></span>
<span data-ttu-id="da608-160">Blob 저장소 계정의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da608-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da608-161">CommonParameters</span></span>
<span data-ttu-id="da608-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da608-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da608-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da608-164">입력</span><span class="sxs-lookup"><span data-stu-id="da608-164">INPUTS</span></span>

### <span data-ttu-id="da608-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da608-165">System.String</span></span>

### <span data-ttu-id="da608-166">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="da608-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="da608-167">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="da608-167">System.Int32</span></span>

### <span data-ttu-id="da608-168">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="da608-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="da608-169">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="da608-169">System.Uri</span></span>

### <span data-ttu-id="da608-170">System.webserver</span><span class="sxs-lookup"><span data-stu-id="da608-170">System.Security.SecureString</span></span>

### <span data-ttu-id="da608-171">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="da608-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="da608-172">출력</span><span class="sxs-lookup"><span data-stu-id="da608-172">OUTPUTS</span></span>

### <span data-ttu-id="da608-173">AutoBackupSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="da608-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="da608-174">상속자</span><span class="sxs-lookup"><span data-stu-id="da608-174">NOTES</span></span>

## <span data-ttu-id="da608-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da608-175">RELATED LINKS</span></span>

[<span data-ttu-id="da608-176">새로운 AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="da608-176">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="da608-177">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="da608-177">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)

