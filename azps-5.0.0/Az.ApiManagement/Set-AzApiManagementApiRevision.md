---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310979"
---
# <span data-ttu-id="f08d0-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f08d0-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="f08d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f08d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f08d0-103">API 수정 버전 수정</span><span class="sxs-lookup"><span data-stu-id="f08d0-103">Modifies an API Revision</span></span>

## <span data-ttu-id="f08d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f08d0-104">SYNTAX</span></span>

### <span data-ttu-id="f08d0-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="f08d0-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f08d0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f08d0-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f08d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f08d0-107">DESCRIPTION</span></span>
<span data-ttu-id="f08d0-108">**AzApiManagementApiRevision** Cmdlet은 Azure API Management api 수정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="f08d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f08d0-109">EXAMPLES</span></span>

### <span data-ttu-id="f08d0-110">예제 1: API 수정 버전 수정</span><span class="sxs-lookup"><span data-stu-id="f08d0-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="f08d0-111">Cmdlet은 `2` `echo-api` 새 설명, 프로토콜 및 경로를 사용 하 여 API의 수정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="f08d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="f08d0-112">PARAMETERS</span></span>

### <span data-ttu-id="f08d0-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f08d0-113">-ApiId</span></span>
<span data-ttu-id="f08d0-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-114">Identifier of existing API.</span></span>
<span data-ttu-id="f08d0-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f08d0-116">-ApiRevision</span></span>
<span data-ttu-id="f08d0-117">기존 API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="f08d0-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="f08d0-119">-AuthorizationScope</span></span>
<span data-ttu-id="f08d0-120">OAuth 작업 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-120">OAuth operations scope.</span></span>
<span data-ttu-id="f08d0-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-121">This parameter is optional.</span></span>
<span data-ttu-id="f08d0-122">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-122">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="f08d0-123">-AuthorizationServerId</span></span>
<span data-ttu-id="f08d0-124">OAuth 권한 부여 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="f08d0-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-125">This parameter is optional.</span></span>
<span data-ttu-id="f08d0-126">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-126">Default value is $null.</span></span>
<span data-ttu-id="f08d0-127">AuthorizationScope가 지정 된 경우이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-127">Must be specified if AuthorizationScope specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="f08d0-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="f08d0-129">API에 액세스 토큰을 전달 하는 데 사용 되는 OpenId 권한 부여 서버 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="f08d0-130">를 참조 http://tools.ietf.org/html/rfc6749#section-4 하세요.</span><span class="sxs-lookup"><span data-stu-id="f08d0-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="f08d0-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-131">This parameter is optional.</span></span> <span data-ttu-id="f08d0-132">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-132">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-133">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f08d0-133">-Context</span></span>
<span data-ttu-id="f08d0-134">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f08d0-135">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-135">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08d0-136">-DefaultProfile</span></span>
<span data-ttu-id="f08d0-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f08d0-138">-설명</span><span class="sxs-lookup"><span data-stu-id="f08d0-138">-Description</span></span>
<span data-ttu-id="f08d0-139">웹 API 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-139">Web API description.</span></span>
<span data-ttu-id="f08d0-140">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-140">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f08d0-141">-InputObject</span></span>
<span data-ttu-id="f08d0-142">PsApiManagementApi의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="f08d0-143">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-144">-이름</span><span class="sxs-lookup"><span data-stu-id="f08d0-144">-Name</span></span>
<span data-ttu-id="f08d0-145">웹 API 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-145">Web API name.</span></span>
<span data-ttu-id="f08d0-146">개발자 및 관리 포털에 표시 되는 API의 공개 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="f08d0-147">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="f08d0-148">-OpenIdProviderId</span></span>
<span data-ttu-id="f08d0-149">OpenId 인증 서버 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="f08d0-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-150">This parameter is optional.</span></span> <span data-ttu-id="f08d0-151">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-151">Default value is $null.</span></span> <span data-ttu-id="f08d0-152">BearerTokenSendingMethods가 지정 된 경우를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f08d0-153">-PassThru</span></span>
<span data-ttu-id="f08d0-154">지정한 경우, set API를 나타내는 ApiManagement의 인스턴스를 PsApiManagementApi 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="f08d0-155">-Path</span><span class="sxs-lookup"><span data-stu-id="f08d0-155">-Path</span></span>
<span data-ttu-id="f08d0-156">웹 API 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-156">Web API Path.</span></span>
<span data-ttu-id="f08d0-157">API 공용 URL의 마지막 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="f08d0-158">이 URL은 웹 서비스에 대 한 요청을 보내기 위해 API 소비자가 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f08d0-159">1 ~ 400 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f08d0-160">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-160">This parameter is optional.</span></span>
<span data-ttu-id="f08d0-161">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-161">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-162">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="f08d0-162">-Protocols</span></span>
<span data-ttu-id="f08d0-163">웹 API 프로토콜 (http, https).</span><span class="sxs-lookup"><span data-stu-id="f08d0-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="f08d0-164">사용할 수 있는 API에 대 한 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="f08d0-165">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-165">This parameter is required.</span></span>
<span data-ttu-id="f08d0-166">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-166">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f08d0-167">-ServiceUrl</span></span>
<span data-ttu-id="f08d0-168">API를 노출 하는 웹 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="f08d0-169">이 URL은 Azure API Management에만 사용 되며 공개 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="f08d0-170">1 ~ 2000 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="f08d0-171">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-171">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-172">-구독 Key이 Ername</span><span class="sxs-lookup"><span data-stu-id="f08d0-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="f08d0-173">구독 키 헤더 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-173">Subscription key header name.</span></span>
<span data-ttu-id="f08d0-174">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-174">This parameter is optional.</span></span>
<span data-ttu-id="f08d0-175">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-175">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="f08d0-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="f08d0-177">구독 키 쿼리 문자열 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="f08d0-178">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-178">This parameter is optional.</span></span>
<span data-ttu-id="f08d0-179">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-179">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08d0-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f08d0-180">-SubscriptionRequired</span></span>
<span data-ttu-id="f08d0-181">Api에 대 한 요청에 SubscriptionRequired 구독을 적용 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="f08d0-182">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="f08d0-183">-확인</span><span class="sxs-lookup"><span data-stu-id="f08d0-183">-Confirm</span></span>
<span data-ttu-id="f08d0-184">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f08d0-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f08d0-185">-WhatIf</span></span>
<span data-ttu-id="f08d0-186">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f08d0-187">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f08d0-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08d0-188">CommonParameters</span></span>
<span data-ttu-id="f08d0-189">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08d0-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08d0-190">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f08d0-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08d0-191">입력</span><span class="sxs-lookup"><span data-stu-id="f08d0-191">INPUTS</span></span>

### <span data-ttu-id="f08d0-192">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f08d0-192">System.String</span></span>

### <span data-ttu-id="f08d0-193">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f08d0-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f08d0-194">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f08d0-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="f08d0-195">ApiManagement [] ServiceManagement. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="f08d0-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="f08d0-196">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f08d0-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f08d0-197">출력</span><span class="sxs-lookup"><span data-stu-id="f08d0-197">OUTPUTS</span></span>

### <span data-ttu-id="f08d0-198">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f08d0-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f08d0-199">상속자</span><span class="sxs-lookup"><span data-stu-id="f08d0-199">NOTES</span></span>

## <span data-ttu-id="f08d0-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f08d0-200">RELATED LINKS</span></span>

[<span data-ttu-id="f08d0-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f08d0-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="f08d0-202">새로운 AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f08d0-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="f08d0-203">제거-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f08d0-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)