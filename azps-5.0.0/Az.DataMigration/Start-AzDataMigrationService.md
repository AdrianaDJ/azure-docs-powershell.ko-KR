---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305345"
---
# <span data-ttu-id="f4da3-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f4da3-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="f4da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4da3-102">SYNOPSIS</span></span>
<span data-ttu-id="f4da3-103">Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="f4da3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4da3-104">SYNTAX</span></span>

### <span data-ttu-id="f4da3-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4da3-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4da3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4da3-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4da3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4da3-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4da3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f4da3-108">DESCRIPTION</span></span>
<span data-ttu-id="f4da3-109">Start-AzDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="f4da3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f4da3-110">EXAMPLES</span></span>

### <span data-ttu-id="f4da3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4da3-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="f4da3-112">위의 예제에서는 입력으로 전달 된 서비스 이름을 기반으로 하는 중지 된 상태의 Test Service 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="f4da3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4da3-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="f4da3-114">위 예제에서는 입력 매개 변수로 전달 된 PSDataMigrationService를 기반으로 Azure 데이터베이스 마이그레이션 서비스 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="f4da3-115">변수</span><span class="sxs-lookup"><span data-stu-id="f4da3-115">PARAMETERS</span></span>

### <span data-ttu-id="f4da3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4da3-116">-DefaultProfile</span></span>
<span data-ttu-id="f4da3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4da3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4da3-118">-InputObject</span></span>
<span data-ttu-id="f4da3-119">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="f4da3-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4da3-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f4da3-120">-Name</span></span>
<span data-ttu-id="f4da3-121">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4da3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4da3-122">-PassThru</span></span>
<span data-ttu-id="f4da3-123">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-123">Returns an true/false.</span></span>
<span data-ttu-id="f4da3-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4da3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4da3-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4da3-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4da3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4da3-127">-ResourceId</span></span>
<span data-ttu-id="f4da3-128">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-128">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4da3-129">-확인</span><span class="sxs-lookup"><span data-stu-id="f4da3-129">-Confirm</span></span>
<span data-ttu-id="f4da3-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4da3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4da3-131">-WhatIf</span></span>
<span data-ttu-id="f4da3-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4da3-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4da3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4da3-134">CommonParameters</span></span>
<span data-ttu-id="f4da3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4da3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4da3-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4da3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4da3-137">입력</span><span class="sxs-lookup"><span data-stu-id="f4da3-137">INPUTS</span></span>

### <span data-ttu-id="f4da3-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f4da3-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="f4da3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f4da3-139">System.String</span></span>

## <span data-ttu-id="f4da3-140">출력</span><span class="sxs-lookup"><span data-stu-id="f4da3-140">OUTPUTS</span></span>

### <span data-ttu-id="f4da3-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f4da3-141">System.Boolean</span></span>

## <span data-ttu-id="f4da3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f4da3-142">NOTES</span></span>

## <span data-ttu-id="f4da3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4da3-143">RELATED LINKS</span></span>