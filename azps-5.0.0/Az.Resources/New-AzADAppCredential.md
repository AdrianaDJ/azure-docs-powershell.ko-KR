---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308777"
---
# <span data-ttu-id="99e8a-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="99e8a-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="99e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="99e8a-103">기존 응용 프로그램에 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="99e8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99e8a-104">SYNTAX</span></span>

### <span data-ttu-id="99e8a-105">ApplicationObjectIdWithPasswordParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="99e8a-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e8a-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e8a-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99e8a-113">설명은</span><span class="sxs-lookup"><span data-stu-id="99e8a-113">DESCRIPTION</span></span>
<span data-ttu-id="99e8a-114">New-AzADAppCredential cmdlet을 사용 하 여 새 자격 증명을 추가 하거나 응용 프로그램에 대 한 자격 증명을 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="99e8a-115">응용 프로그램은 응용 프로그램 개체 id 또는 응용 프로그램 Id 중 하나를 제공 하 여 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="99e8a-116">예제의</span><span class="sxs-lookup"><span data-stu-id="99e8a-116">EXAMPLES</span></span>

### <span data-ttu-id="99e8a-117">예제 1-암호를 사용 하 여 새 응용 프로그램 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="99e8a-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="99e8a-118">새 암호 자격 증명이 개체 id가 ' 1f89cf81-0146-4f4e-beae-2007d0668416 ' 인 기존 응용 프로그램에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="99e8a-119">예제 2-인증서를 사용 하 여 새 응용 프로그램 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="99e8a-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="99e8a-120">제공 된 base64로 인코딩된 공개 X509 인증서 ("myapp.exe")가 응용 프로그램 id가 ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 ' 인 기존 응용 프로그램에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="99e8a-121">예제 3-파이핑을 사용 하 여 새 응용 프로그램 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="99e8a-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="99e8a-122">개체 id가 ' 1f89cf81-0146-4f4e-beae-2007d0668416 ' 인 응용 프로그램을 가져오고 지정 된 암호를 사용 하 여 해당 응용 프로그램에 대 한 새 응용 프로그램 자격 증명을 만들기 위해 New-AzADAppCredential에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="99e8a-123">변수</span><span class="sxs-lookup"><span data-stu-id="99e8a-123">PARAMETERS</span></span>

### <span data-ttu-id="99e8a-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="99e8a-124">-ApplicationId</span></span>
<span data-ttu-id="99e8a-125">자격 증명을 추가할 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="99e8a-126">-ApplicationObject</span></span>
<span data-ttu-id="99e8a-127">자격 증명을 추가할 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="99e8a-128">-CertValue</span></span>
<span data-ttu-id="99e8a-129">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="99e8a-130">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e8a-131">-DefaultProfile</span></span>
<span data-ttu-id="99e8a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99e8a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99e8a-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99e8a-133">-DisplayName</span></span>
<span data-ttu-id="99e8a-134">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="99e8a-135">-EndDate</span></span>
<span data-ttu-id="99e8a-136">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="99e8a-137">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="99e8a-138">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="99e8a-139">-ObjectId</span></span>
<span data-ttu-id="99e8a-140">자격 증명을 추가할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-141">-암호</span><span class="sxs-lookup"><span data-stu-id="99e8a-141">-Password</span></span>
<span data-ttu-id="99e8a-142">응용 프로그램과 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-143">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="99e8a-143">-StartDate</span></span>
<span data-ttu-id="99e8a-144">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="99e8a-145">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-145">The default start date value is today.</span></span> <span data-ttu-id="99e8a-146">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e8a-147">-확인</span><span class="sxs-lookup"><span data-stu-id="99e8a-147">-Confirm</span></span>
<span data-ttu-id="99e8a-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e8a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e8a-149">-WhatIf</span></span>
<span data-ttu-id="99e8a-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e8a-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e8a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e8a-152">CommonParameters</span></span>
<span data-ttu-id="99e8a-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e8a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e8a-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99e8a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e8a-155">입력</span><span class="sxs-lookup"><span data-stu-id="99e8a-155">INPUTS</span></span>

### <span data-ttu-id="99e8a-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99e8a-156">System.String</span></span>

### <span data-ttu-id="99e8a-157">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="99e8a-157">System.Guid</span></span>

### <span data-ttu-id="99e8a-158">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="99e8a-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="99e8a-159">System.webserver</span><span class="sxs-lookup"><span data-stu-id="99e8a-159">System.Security.SecureString</span></span>

### <span data-ttu-id="99e8a-160">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="99e8a-160">System.DateTime</span></span>

## <span data-ttu-id="99e8a-161">출력</span><span class="sxs-lookup"><span data-stu-id="99e8a-161">OUTPUTS</span></span>

### <span data-ttu-id="99e8a-162">ActiveDirectory Adcredential 자격 증명</span><span class="sxs-lookup"><span data-stu-id="99e8a-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="99e8a-163">상속자</span><span class="sxs-lookup"><span data-stu-id="99e8a-163">NOTES</span></span>

## <span data-ttu-id="99e8a-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99e8a-164">RELATED LINKS</span></span>

[<span data-ttu-id="99e8a-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="99e8a-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="99e8a-166">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="99e8a-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="99e8a-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="99e8a-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
