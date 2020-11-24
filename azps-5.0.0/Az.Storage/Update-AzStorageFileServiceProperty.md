---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310556"
---
# <span data-ttu-id="edd4f-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="edd4f-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="edd4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="edd4f-103">Azure 저장소 파일 서비스에 대 한 서비스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="edd4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="edd4f-104">SYNTAX</span></span>

### <span data-ttu-id="edd4f-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="edd4f-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edd4f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="edd4f-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edd4f-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="edd4f-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edd4f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="edd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="edd4f-109">**업데이트 AzStorageFileServiceProperty** Cmdlet은 Azure 저장소 파일 서비스의 서비스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="edd4f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="edd4f-110">EXAMPLES</span></span>

### <span data-ttu-id="edd4f-111">예제 1: 파일 공유 소프트 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="edd4f-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="edd4f-112">이 명령은 보존 날짜가 5 인 파일 공유 소프트 삭제 삭제를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="edd4f-113">변수</span><span class="sxs-lookup"><span data-stu-id="edd4f-113">PARAMETERS</span></span>

### <span data-ttu-id="edd4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd4f-114">-DefaultProfile</span></span>
<span data-ttu-id="edd4f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd4f-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="edd4f-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="edd4f-117">저장소 계정에 대 한 공유 삭제 보존 정책 사용 $true으로 설정 하 여 $false로 설정 된 공유 삭제 보존 정책 사용을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd4f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd4f-118">-ResourceGroupName</span></span>
<span data-ttu-id="edd4f-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd4f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edd4f-120">-ResourceId</span></span>
<span data-ttu-id="edd4f-121">저장소 계정 리소스 Id 또는 파일 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edd4f-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="edd4f-122">-ShareRetentionDays</span></span>
<span data-ttu-id="edd4f-123">공유 DeleteRetentionPolicy 보존 일 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="edd4f-124">공유 삭제 보존 정책을 사용 하도록 설정한 경우에만 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd4f-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="edd4f-125">-StorageAccount</span></span>
<span data-ttu-id="edd4f-126">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="edd4f-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edd4f-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="edd4f-127">-StorageAccountName</span></span>
<span data-ttu-id="edd4f-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd4f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="edd4f-129">-Confirm</span></span>
<span data-ttu-id="edd4f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd4f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd4f-131">-WhatIf</span></span>
<span data-ttu-id="edd4f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd4f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd4f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd4f-134">CommonParameters</span></span>
<span data-ttu-id="edd4f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd4f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd4f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd4f-137">입력</span><span class="sxs-lookup"><span data-stu-id="edd4f-137">INPUTS</span></span>

### <span data-ttu-id="edd4f-138">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edd4f-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="edd4f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="edd4f-139">System.String</span></span>

## <span data-ttu-id="edd4f-140">출력</span><span class="sxs-lookup"><span data-stu-id="edd4f-140">OUTPUTS</span></span>

### <span data-ttu-id="edd4f-141">PSFileServiceProperties를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd4f-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="edd4f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="edd4f-142">NOTES</span></span>

## <span data-ttu-id="edd4f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edd4f-143">RELATED LINKS</span></span>