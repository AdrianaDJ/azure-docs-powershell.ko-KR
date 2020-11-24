---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305420"
---
# <span data-ttu-id="ad385-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="ad385-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="ad385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad385-102">SYNOPSIS</span></span>
<span data-ttu-id="ad385-103">Azure ActiveDirectory 응용 프로그램 세부 정보를 DataMigration 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad385-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="ad385-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad385-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad385-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad385-105">DESCRIPTION</span></span>
<span data-ttu-id="ad385-106">Azure ActiveDirectory 응용 프로그램 세부 정보를 DataMigration 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad385-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="ad385-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad385-107">EXAMPLES</span></span>

### <span data-ttu-id="ad385-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad385-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="ad385-109">ApplicationId: "사용자의 AppId/서비스 사용자 Id" AppKey: System.webserver TenantId: "테 넌 트 Id"</span><span class="sxs-lookup"><span data-stu-id="ad385-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="ad385-110">변수</span><span class="sxs-lookup"><span data-stu-id="ad385-110">PARAMETERS</span></span>

### <span data-ttu-id="ad385-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="ad385-111">-AppKey</span></span>
<span data-ttu-id="ad385-112">Azure Active Directory 키</span><span class="sxs-lookup"><span data-stu-id="ad385-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad385-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ad385-113">-ApplicationId</span></span>
<span data-ttu-id="ad385-114">Azure Active Directory 응용 프로그램 Id</span><span class="sxs-lookup"><span data-stu-id="ad385-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad385-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad385-115">-DefaultProfile</span></span>
<span data-ttu-id="ad385-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad385-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad385-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad385-117">CommonParameters</span></span>
<span data-ttu-id="ad385-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad385-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ad385-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad385-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad385-120">입력</span><span class="sxs-lookup"><span data-stu-id="ad385-120">INPUTS</span></span>

### <span data-ttu-id="ad385-121">않아야</span><span class="sxs-lookup"><span data-stu-id="ad385-121">None</span></span>

## <span data-ttu-id="ad385-122">출력</span><span class="sxs-lookup"><span data-stu-id="ad385-122">OUTPUTS</span></span>

### <span data-ttu-id="ad385-123">DataMigration. PSAzureActiveDirectoryApp/.</span><span class="sxs-lookup"><span data-stu-id="ad385-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="ad385-124">상속자</span><span class="sxs-lookup"><span data-stu-id="ad385-124">NOTES</span></span>

## <span data-ttu-id="ad385-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad385-125">RELATED LINKS</span></span>