---
title: "&lt;AppContextSwitchOverrides&gt; 요소"
ms.custom: 
ms.date: 10/17/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-bcl
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- AppContextSwitchOverrides
- compatibility switches
- configuration switches
- configuration
ms.assetid: 4ce07f47-7ddb-4d91-b067-501bd8b88752
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9ed1b11cef909af153e43d61e71a4875648bdbfb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="ltappcontextswitchoverridesgt-element"></a><span data-ttu-id="75959-102">&lt;AppContextSwitchOverrides&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="75959-102">&lt;AppContextSwitchOverrides&gt; Element</span></span>
<span data-ttu-id="75959-103"><xref:System.AppContext> 클래스에 사용되는 스위치를 하나 이상 정의하여 새 기능의 옵트아웃 메커니즘을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-103">Defines one or more switches used by the <xref:System.AppContext> class to provide an opt-out mechanism for new functionality.</span></span>  
  
 <span data-ttu-id="75959-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="75959-104">\<configuration></span></span>  
 <span data-ttu-id="75959-105">\<런타임 ></span><span class="sxs-lookup"><span data-stu-id="75959-105">\<runtime></span></span>  
<span data-ttu-id="75959-106">\<AppContextSwitchOverrides ></span><span class="sxs-lookup"><span data-stu-id="75959-106">\<AppContextSwitchOverrides></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75959-107">구문</span><span class="sxs-lookup"><span data-stu-id="75959-107">Syntax</span></span>  
  
```xml  
<AppContextSwitchOverrides value="name1=value1[[;name2=value2];...]" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="75959-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="75959-108">Attributes and Elements</span></span>  
 <span data-ttu-id="75959-109">다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="75959-110">특성</span><span class="sxs-lookup"><span data-stu-id="75959-110">Attributes</span></span>  
  
|<span data-ttu-id="75959-111">특성</span><span class="sxs-lookup"><span data-stu-id="75959-111">Attribute</span></span>|<span data-ttu-id="75959-112">설명</span><span class="sxs-lookup"><span data-stu-id="75959-112">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="75959-113">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="75959-114">하나 이상의 스위치 이름 및 연결 된 부울 값을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-114">Defines one or more switch names and their associated Boolean values.</span></span>|  
  
### <a name="value-attribute"></a><span data-ttu-id="75959-115">특성 값</span><span class="sxs-lookup"><span data-stu-id="75959-115">value Attribute</span></span>  
  
|<span data-ttu-id="75959-116">값</span><span class="sxs-lookup"><span data-stu-id="75959-116">Value</span></span>|<span data-ttu-id="75959-117">설명</span><span class="sxs-lookup"><span data-stu-id="75959-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="75959-118">"name = value"</span><span class="sxs-lookup"><span data-stu-id="75959-118">"name=value"</span></span>|<span data-ttu-id="75959-119">미리 정의 된 스위치 이름과 해당 값 (`true` 또는 `false`).</span><span class="sxs-lookup"><span data-stu-id="75959-119">A predefined switch name along with its value (`true` or `false`).</span></span> <span data-ttu-id="75959-120">여러 스위치 이름/값 쌍은 세미콜론으로 구분 됩니다 (";").</span><span class="sxs-lookup"><span data-stu-id="75959-120">Multiple switch name/value pairs are separated by semicolons (";").</span></span> <span data-ttu-id="75959-121">.NET Framework에서 지원 되는 미리 정의 된 스위치 이름 목록은 설명 섹션을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-121">For a list of predefined switch names supported by the .NET Framework, see the Remarks section.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="75959-122">자식 요소</span><span class="sxs-lookup"><span data-stu-id="75959-122">Child Elements</span></span>  
 <span data-ttu-id="75959-123">없음</span><span class="sxs-lookup"><span data-stu-id="75959-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="75959-124">부모 요소</span><span class="sxs-lookup"><span data-stu-id="75959-124">Parent Elements</span></span>  
  
|<span data-ttu-id="75959-125">요소</span><span class="sxs-lookup"><span data-stu-id="75959-125">Element</span></span>|<span data-ttu-id="75959-126">설명</span><span class="sxs-lookup"><span data-stu-id="75959-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="75959-127">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="75959-128">런타임 초기화 옵션에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-128">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="75959-129">설명</span><span class="sxs-lookup"><span data-stu-id="75959-129">Remarks</span></span>  
 <span data-ttu-id="75959-130">.NET Framework 4.6부터는 `<AppContextSwitchOverrides>` 앱 새 기능을 사용 하거나 라이브러리의 이전 버전과 호환성을 유지 수 있는지 여부를 확인 하려면 API의 호출자를 허용 하는 구성 파일의 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-130">Starting with the .NET Framework 4.6, the `<AppContextSwitchOverrides>` element in a configuration file allows callers of an API to determine whether their app can take advantage of new functionality or preserve compatibility with previous versions of a library.</span></span> <span data-ttu-id="75959-131">예를 들어, API의 동작을 라이브러리의 두 버전 간의 변경 된 경우는 `<AppContextSwitchOverrides>` 요소 라이브러리의 새로운 기능을 지 원하는 버전에 새 동작을 취소 하기 위해 해당 API의 호출자를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-131">For example, if the behavior of an API has changed between two versions of a library, the `<AppContextSwitchOverrides>` element allows callers of that API to opt out of the new behavior on versions of the library that support the new functionality.</span></span> <span data-ttu-id="75959-132">.NET framework에서 Api를 호출 하는 앱에 대 한는 `<AppContextSwitchOverrides>` 요소 호출자가 해당 앱을 이전 버전의.NET Framework 앱의 포함 하는.NET Framework 버전에서 실행 중인 경우에 새로운 기능을 선택 하도록 대상 수 있습니다 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-132">For apps that call APIs in the .NET Framework, the `<AppContextSwitchOverrides>` element can also allow callers whose apps target an earlier version of the .NET Framework to opt into new functionality if their app is running on a version of the .NET Framework that includes that functionality.</span></span>  
  
 <span data-ttu-id="75959-133">`value` 의 특성은 `<AppContextSwitchOverrides>` 요소는 하나 이상의 세미콜론으로 구분 된 이름/값 쌍으로 구성 된 단일 문자열을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-133">The `value` attribute of the `<AppContextSwitchOverrides>` element consists of a single string that consists of one or more semicolon-delimited name/value pairs.</span></span>  <span data-ttu-id="75959-134">각 이름은 호환성 스위치를 식별 하 고 해당 값은 부울 (`true` 또는 `false`) 스위치가 설정 되어 있는지 여부를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-134">Each name identifies a compatibility switch, and its corresponding value is a Boolean (`true` or `false`) that indicates whether the switch is set.</span></span> <span data-ttu-id="75959-135">스위치는 기본적으로 `false`, 라이브러리의 새로운 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-135">By default, the switch is `false`, and libraries  provide the new functionality.</span></span> <span data-ttu-id="75959-136">스위치가 설정 되어 있으면만 이전 기능 제공 (즉, 해당 값은 `true`).</span><span class="sxs-lookup"><span data-stu-id="75959-136">They only provide the previous functionality if the switch is set (that is, its value is `true`).</span></span> <span data-ttu-id="75959-137">이렇게 하면 라이브러리의 새로운 기능을 취소 하기 위해 이전 동작에 의존 하는 호출자를 허용 하면서 기존 API에 대 한 새 동작을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75959-137">This allows libraries to provide new behavior for an existing API while allowing callers who depend on the previous behavior to opt out of the new functionality.</span></span>  
  
 <span data-ttu-id="75959-138">.NET Framework에서는 다음 스위치를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-138">The .NET Framework supports the following switches:</span></span>  
  
|<span data-ttu-id="75959-139">스위치 이름</span><span class="sxs-lookup"><span data-stu-id="75959-139">Switch name</span></span>|<span data-ttu-id="75959-140">설명</span><span class="sxs-lookup"><span data-stu-id="75959-140">Description</span></span>|<span data-ttu-id="75959-141">도입</span><span class="sxs-lookup"><span data-stu-id="75959-141">Introduced</span></span>|  
|-----------------|-----------------|----------------|  
|`Switch.MS.Internal.`<br/>`DoNotApplyLayoutRoundingToMarginsAndBorderThickness`|<span data-ttu-id="75959-142">Windows Presentation Foundation 컨트롤 레이아웃에 대 한 레거시 알고리즘을 사용 하는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-142">Controls whether Windows Presentation Foundation uses legacy a algorithm for control layout.</span></span> <span data-ttu-id="75959-143">자세한 내용은 [완화: WPF 레이아웃](~/docs/framework/migration-guide/mitigation-wpf-layout.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="75959-143">For more information, see [Mitigation: WPF Layout](~/docs/framework/migration-guide/mitigation-wpf-layout.md).</span></span>|<span data-ttu-id="75959-144">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-144">.NET Framework 4.6</span></span>|  
|`Switch.System.Activities.`<br/>`UseMD5CryptoServiceProviderForWFDebugger`|<span data-ttu-id="75959-145">로 설정 하면 `false`, FIPS가 설정 된 경우 Visual Studio를 사용 하 여 XAML 기반 워크플로 프로젝트를 디버깅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75959-145">When set to `false`, allows debugging of XAML-based workflow projects with Visual Studio when FIPS is enabled.</span></span> <span data-ttu-id="75959-146">없으면는 <xref:System.NullReferenceException> System.Activities 어셈블리의 메서드 호출에서 throw 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75959-146">Without it, a <xref:System.NullReferenceException> is thrown in calls to methods in the System.Activities assembly.</span></span>|<span data-ttu-id="75959-147">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-147">.NET Framework 4.7</span></span>|
|`Switch.System.Drawing.`<br/>`DontSupportPngFramesInIcons`|<span data-ttu-id="75959-148">컨트롤 여부는 <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> 메서드에서 예외가 throw 때는 <xref:System.Drawing.Icon> 개체에 PNG 프레임이 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-148">Controls whether the <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> method throws an exception when an <xref:System.Drawing.Icon> object has PNG frames.</span></span> <span data-ttu-id="75959-149">자세한 내용은 [완화: 아이콘 개체의 PNG 프레임](~/docs/framework/migration-guide/mitigation-png-frames-in-icon-objects.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="75959-149">For more information, see [Mitigation: PNG Frames in Icon Objects](~/docs/framework/migration-guide/mitigation-png-frames-in-icon-objects.md).</span></span>|<span data-ttu-id="75959-150">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-150">.NET Framework 4.6</span></span>|  
|`Switch.System.Globalization.NoAsyncCurrentCulture`|<span data-ttu-id="75959-151">비동기 작업 호출 스레드의 컨텍스트를 전달 하지 않는 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-151">Controls whether asynchronous operations do not flow from the calling thread's context.</span></span> <span data-ttu-id="75959-152">자세한 내용은 참조 [CurrentCulture 및 CurrentUICulture 흐름 태스크에 걸쳐](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#currentculture-and-currentuiculture-flow-across-tasks)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-152">For more information, see [CurrentCulture and CurrentUICulture flow across tasks](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#currentculture-and-currentuiculture-flow-across-tasks).</span></span>|<span data-ttu-id="75959-153">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-153">.NET Framework 4.6</span></span>|  
|`Switch.System.IdentityModel.`<br/>`DisableMultipleDNSEntriesInSANCertificate`|<span data-ttu-id="75959-154">컨트롤 여부는 <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims%2A?displayProperty=nameWithType> 메서드 클레임 유형을 마지막 DNS 항목만 일치 시 키 려 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-154">Controls whether the <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims%2A?displayProperty=nameWithType> method attempts to match the claim type only with the last DNS entry.</span></span> <span data-ttu-id="75959-155">자세한 내용은 [완화: X509CertificateClaimSet.FindClaims 메서드](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="75959-155">For more information, see [Mitigation: X509CertificateClaimSet.FindClaims Method](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md).</span></span>|<span data-ttu-id="75959-156">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="75959-156">.NET Framework 4.6.1</span></span>|  
|`Switch.System.IO.BlockLongPaths`|<span data-ttu-id="75959-157">컨트롤 있는지 여부를 보다 긴 경로 `MAX_PATH` (260 자)를 throw 한 <xref:System.IO.PathTooLongException>합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-157">Controls whether paths longer than `MAX_PATH` (260 characters) throw a <xref:System.IO.PathTooLongException>.</span></span> <span data-ttu-id="75959-158">자세한 내용은 참조 [긴 경로 지원](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#long-path-support)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-158">For more information, see [Long Path Support](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#long-path-support).</span></span>|<span data-ttu-id="75959-159">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="75959-159">.NET Framework 4.6.2</span></span>|  
|`Switch.System.IO.Compression.ZipFile.`<br/>`UseBackslash`|<span data-ttu-id="75959-160">백슬래시를 사용 하 여 ("\\") 대신 슬래시 ("/")로 경로 구분 기호에는 <xref:System.IO.Compression.ZipArchiveEntry.FullName%2A?displayProperty=nameWithType> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-160">Uses the backslash ("\\") rather than the forward slash ("/") as the path separator in the <xref:System.IO.Compression.ZipArchiveEntry.FullName%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="75959-161">자세한 내용은 참조 [완화: ZipArchiveEntry.FullName 경로 구분 기호](~/docs/framework/migration-guide/mitigation-ziparchiveentry-fullname-path-separator.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-161">For more information, see  [Mitigation: ZipArchiveEntry.FullName Path Separator](~/docs/framework/migration-guide/mitigation-ziparchiveentry-fullname-path-separator.md).</span></span>|<span data-ttu-id="75959-162">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="75959-162">.NET Framework 4.6.1</span></span>|  
|`Switch.System.IO.`<br/>`UseLegacyPathHandling`|<span data-ttu-id="75959-163">레거시 경로 정규화 사용 되 고 URI 경로에서 사용할 수 있는지 여부를 제어는 <xref:System.IO.Path.GetDirectoryName%2A?displayProperty=nameWithType> 및 <xref:System.IO.Path.GetPathRoot%2A?displayProperty=nameWithType> 메서드.</span><span class="sxs-lookup"><span data-stu-id="75959-163">Controls whether legacy path normalization is used and URI paths are supported by the <xref:System.IO.Path.GetDirectoryName%2A?displayProperty=nameWithType> and <xref:System.IO.Path.GetPathRoot%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="75959-164">자세한 내용은 참조 [완화: 경로 정규화](~/docs/framework/migration-guide/mitigation-path-normalization.md) 및 [완화: 경로 콜론 검사](~/docs/framework/migration-guide/mitigation-path-colon-checks.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-164">For more information, see [Mitigation: Path Normalization](~/docs/framework/migration-guide/mitigation-path-normalization.md) and [Mitigation: Path Colon Checks](~/docs/framework/migration-guide/mitigation-path-colon-checks.md).</span></span>|<span data-ttu-id="75959-165">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="75959-165">.NET Framework 4.6.2</span></span>|  
|`Switch.System.`<br/>`MemberDescriptorEqualsReturnsFalseIfEquivalent`|<span data-ttu-id="75959-166">같음 비교에 대 한 테스트가 있는지 여부를 제어는 <xref:System.ComponentModel.MemberDescriptor.Category%2A?displayProperty=nameWithType> 한 개체의 속성은 <xref:System.ComponentModel.MemberDescriptor.Description%2A?displayProperty=nameWithType> 두 번째 개체의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-166">Controls whether a test for equality compares the <xref:System.ComponentModel.MemberDescriptor.Category%2A?displayProperty=nameWithType> property of one object with the <xref:System.ComponentModel.MemberDescriptor.Description%2A?displayProperty=nameWithType> property of the second object.</span></span> <span data-ttu-id="75959-167">자세한 내용은 참조 [MemberDescriptor.Equals 잘못 구현](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#incorrect-implementation-of-memberdescriptorequals)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-167">For more information, see [Incorrect implementation of MemberDescriptor.Equals](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#incorrect-implementation-of-memberdescriptorequals).</span></span>|<span data-ttu-id="75959-168">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="75959-168">.NET Framework 4.6.2</span></span>|  
 `Switch.System.Net.`<br/>`DontCheckCertificateEKUs`|<span data-ttu-id="75959-169">인증서 확장 된 키 사용 (EKU) 개체 식별자 (OID) 유효성 검사를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75959-169">Disables certificate enhanced key usage (EKU) object identifier (OID) validation.</span></span> <span data-ttu-id="75959-170">(Eku 확장) 확장 된 키 사용 확장은 키를 사용 하는 응용 프로그램을 나타내는 개체 식별자 (Oid)의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-170">An enhanced key usage (EKU) extension is a collection of object identifiers (OIDs) that indicate the applications that use the key.</span></span>|<span data-ttu-id="75959-171">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-171">.NET Framework 4.6</span></span>|
|`Switch.System.Net.`<br/>`DontEnableSchSendAuxRecord`|<span data-ttu-id="75959-172">SCH_SEND_AUX_RECORD의 사용을 비활성화 하 여 완화 방법은 TLS1.0 브라우저 악용에 대해 SSL/TLS (비스 트)를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-172">Disables TLS1.0 Browser Exploit Against SSL/TLS (BEAST) mitigation by disabling the use of SCH_SEND_AUX_RECORD.</span></span>|<span data-ttu-id="75959-173">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-173">.NET Framework 4.6</span></span>|
|`Switch.System.Net.`<br/>`DontEnableSchUseStrongCrypto`|<span data-ttu-id="75959-174">컨트롤 여부는 <xref:System.Net.ServicePointManager?displayProperty=nameWithType> 및 <xref:System.Net.Security.SslStream?displayProperty=nameWithType> 클래스는 SSL 3.0 프로토콜을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75959-174">Controls whether the <xref:System.Net.ServicePointManager?displayProperty=nameWithType> and <xref:System.Net.Security.SslStream?displayProperty=nameWithType> classes can use the SSL 3.0 protocol.</span></span> <span data-ttu-id="75959-175">자세한 내용은 [완화: TLS 프로토콜](~/docs/framework/migration-guide/mitigation-tls-protocols.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="75959-175">For more information, see [Mitigation: TLS Protocols](~/docs/framework/migration-guide/mitigation-tls-protocols.md).</span></span>|<span data-ttu-id="75959-176">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-176">.NET Framework 4.6</span></span>|
|`Switch.System.Net.`<br/>`DontEnableSystemDefaultTlsVersions`|<span data-ttu-id="75959-177">기본값은 t l s 12, Tls11, Tls 되돌립니다 SystemDefault TLS 버전을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-177">Disables SystemDefault TLS versions reverting back to a default of Tls12, Tls11, Tls.</span></span>|<span data-ttu-id="75959-178">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-178">.NET Framework 4.7</span></span>|
|`Switch.System.Net.`<br/>`DontEnableTlsAlerts`|<span data-ttu-id="75959-179">SslStream TLS 서버 쪽 경고를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-179">Disables SslStream TLS server-side Alerts.</span></span>|<span data-ttu-id="75959-180">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-180">.NET Framework 4.7</span></span>|
|`Switch.System.Runtime.Serialization.`<br/>`DoNotUseECMAScriptV6EscapeControlCharacter` |<span data-ttu-id="75959-181">컨트롤 여부는 [DataContractJsonSerializer](xref:System.Runtime.Serialization.Json.DataContractJsonSerializer) ECMAScript V6 및 V8 표준에 따라 일부 제어 문자를 serialize 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-181">Controls whether the [DataContractJsonSerializer](xref:System.Runtime.Serialization.Json.DataContractJsonSerializer) serializes some control characters based on the ECMAScript V6 and V8 standards.</span></span> <span data-ttu-id="75959-182">자세한 내용은 [완화: DataContractJsonSerializer로 제어 문자 serialization](Mitigation:%20Serialization%20of%20Control%20Characters%20with%20the%20DataContractJsonSerializer.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75959-182">For more information, see [Mitigation: Serialization of Control Characters with the DataContractJsonSerializer](Mitigation:%20Serialization%20of%20Control%20Characters%20with%20the%20DataContractJsonSerializer.md)</span></span>| <span data-ttu-id="75959-183">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-183">.NET Framework 4.7</span></span> |
|`Switch.System.Security.ClaimsIdentity.`<br/>`SetActorAsReferenceWhenCopyingClaimsIdentity`|<span data-ttu-id="75959-184">컨트롤 여부는 <xref:System.Security.Claims.ClaimsIdentity.%23ctor%28System.Security.Principal.IIdentity%29?displayProperty=nameWithType> 생성자는 새 개체의 설정 <xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=nameWithType> 기존 개체 참조를 사용 하 여 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-184">Controls whether the <xref:System.Security.Claims.ClaimsIdentity.%23ctor%28System.Security.Principal.IIdentity%29?displayProperty=nameWithType> constructor sets the  new object's <xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=nameWithType> property with an existing object reference.</span></span> <span data-ttu-id="75959-185">자세한 내용은 [완화: ClaimsIdentity 생성자](~/docs/framework/migration-guide/mitigation-claimsidentity-constructor.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75959-185">For more information, see [Mitigation: ClaimsIdentity Constructor](~/docs/framework/migration-guide/mitigation-claimsidentity-constructor.md).</span></span>|<span data-ttu-id="75959-186">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="75959-186">.NET Framework 4.6.2</span></span>|  
|`Switch.System.Security.Cryptography.`<br/>`AesCryptoServiceProvider.DontCorrectlyResetDecryptor`|<span data-ttu-id="75959-187">컨트롤 있는지 여부를 다시 사용 하려고는 <xref:System.Security.Cryptography.AesCryptoServiceProvider> 암호 해독기를 throw 한 <xref:System.Security.Cryptography.CryptographicException>합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-187">Controls whether the attempt to reuse an <xref:System.Security.Cryptography.AesCryptoServiceProvider> decryptor throws a <xref:System.Security.Cryptography.CryptographicException>.</span></span> <span data-ttu-id="75959-188">자세한 내용은 AesCryptoServiceProvider 암호 해독기를 재사용 가능한 transform](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#aescryptoserviceprovider-decryptor-provides-a-reusable-transform) 제공을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="75959-188">For more information, see AesCryptoServiceProvider decryptor provides a reusable transform](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#aescryptoserviceprovider-decryptor-provides-a-reusable-transform).</span></span>|<span data-ttu-id="75959-189">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="75959-189">.NET Framework 4.6.2</span></span>|
|`Switch.System.Security.Cryptography.`<br/>`DoNotAddrOfCspParentWindowHandle`|<span data-ttu-id="75959-190">컨트롤 여부의 값은 [CspParameters.ParentWindowHandle](xref:System.Security.Cryptography.CspParameters.ParentWindowHandle) 속성은는 [IntPtr](xref:System.IntPtr) 창의 메모리 위치 처리할 나타냅니다 또는 창 핸들 (HWND) 인지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-190">Controls whether the value of the [CspParameters.ParentWindowHandle](xref:System.Security.Cryptography.CspParameters.ParentWindowHandle) property is an [IntPtr](xref:System.IntPtr) that represents the memory location of a window handle, or whether it is a window handle (an HWND).</span></span> <span data-ttu-id="75959-191">자세한 내용은 [완화: CspParameters.ParentWindowHandle에 HWND 필요](Mitigation:%20CspParameters.ParentWindowHandle%20Expects%20an%20HWND.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75959-191">For more information, see [Mitigation: CspParameters.ParentWindowHandle Expects an HWND](Mitigation:%20CspParameters.ParentWindowHandle%20Expects%20an%20HWND.md).</span></span> |<span data-ttu-id="75959-192">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-192">.NET Framework 4.7</span></span>|   
|`Switch.System.ServiceModel.`<br/>`AllowUnsignedToHeader`|<span data-ttu-id="75959-193">결정 여부는 `TransportWithMessageCredential` 보안 모드에서는 메시지를 부호 없는 "to" 헤더가 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-193">Determines whether the `TransportWithMessageCredential` security mode allows messages with an unsigned "to" header.</span></span> <span data-ttu-id="75959-194">옵트인 스위치입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-194">This is an opt-in switch.</span></span> <span data-ttu-id="75959-195">자세한 내용은 참조 [.NET Framework 4.6.1의에서 런타임 변경 내용](https://msdn.microsoft.com/library/mt592686.aspx#WCF)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-195">For more information, see [Runtime Changes in the .NET Framework 4.6.1](https://msdn.microsoft.com/library/mt592686.aspx#WCF).</span></span>|<span data-ttu-id="75959-196">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="75959-196">.NET Framework 4.6.1</span></span>| 
|`Switch.System.ServiceModel.`<br />`DisableCngCertificates`|<span data-ttu-id="75959-197">CSG 키 저장소 공급자 예외가 throw X509 사용 시도가 함께 인증서 있는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-197">Determines whether the attempt to use X509 certificates with a CSG key storage provider throws an exception.</span></span> <span data-ttu-id="75959-198">자세한 내용은 참조 [WCF 전송 보안 지원 CNG를 사용 하 여 저장 된 인증서를](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#wcf-transport-security-supports-certificates-stored-using-cng)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-198">For more information, see [WCF transport security supports certificates stored using CNG](~/docs/framework/migration-guide/retargeting/4.6.1-4.6.2.md#wcf-transport-security-supports-certificates-stored-using-cng).</span></span>|<span data-ttu-id="75959-199">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="75959-199">.NET Framework 4.6.1</span></span>|
|`Switch.System.ServiceModel.`<br/>`DisableUsingServicePointManagerSecurityProtocols`|<span data-ttu-id="75959-200">와 함께 `Switch.System.Net.DontEnableSchUseStrongCrypto`, TLS 1.1 및 TLS 1.2 WCF 메시지 보안을 사용할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-200">Along with `Switch.System.Net.DontEnableSchUseStrongCrypto`, determines whether WCF message security uses TLS 1.1 and TLS 1.2.</span></span>|<span data-ttu-id="75959-201">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-201">.NET Framework 4.7</span></span> |    
|`Switch.System.Windows.Controls.Grid.`<br/>`StarDefinitionsCanExceedAvailableSpace` |<span data-ttu-id="75959-202">Windows Presentation Foundation 오래 된 알고리즘에 적용 되는지 여부를 결정 (`true`) 또는 새 알고리즘 (`false`)에서 공간을 할당 \*-열입니다.</span><span class="sxs-lookup"><span data-stu-id="75959-202">Determines whether Windows Presentation Foundation applies an old algorithm (`true`) or a new algorithm (`false`) in allocating space to \*-columns.</span></span> <span data-ttu-id="75959-203">자세한 내용은 [완화: Grid 컨트롤의 별 열 공간 할당](Mitigation:%20Grid%20Control's%20Space%20Allocation%20to%20Star-columns.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75959-203">For more information, see [Mitigation: Grid Control's Space Allocation to Star-columns](Mitigation:%20Grid%20Control's%20Space%20Allocation%20to%20Star-columns.md).</span></span> |<span data-ttu-id="75959-204">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-204">.NET Framework 4.7</span></span> |
|`Switch.System.Windows.Forms.`<br />`DontSupportReentrantFilterMessage`|<span data-ttu-id="75959-205">사용자 지정을 허용 하는 코드 opts <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A?displayProperty=nameWithType> 예외를 throw 하지 않고 메시지를 안전 하 게 필터링 하는 구현 때는 <xref:System.Windows.Forms.Application.FilterMessage%2A?displayProperty=nameWithType> 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-205">Opts out of the code that allows a custom <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A?displayProperty=nameWithType> implementation to safely filter messages without throwing an exception when the <xref:System.Windows.Forms.Application.FilterMessage%2A?displayProperty=nameWithType> method is called.</span></span> <span data-ttu-id="75959-206">자세한 내용은 [완화: 사용자 지정 IMessageFilter.PreFilterMessage 구현](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="75959-206">For more information, see [Mitigation: Custom IMessageFilter.PreFilterMessage Implementations](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md).</span></span>|<span data-ttu-id="75959-207">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="75959-207">.NET Framework 4.6.1</span></span>|  
|`Switch.System.Windows.Input.Stylus.`<br/>`EnablePointerSupport`|<span data-ttu-id="75959-208">여부, 선택적 `WM_POINTER`-기반된 터치/스타일러스 스택을 WPF 응용 프로그램에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75959-208">Determines whether an optional `WM_POINTER`-based touch/stylus stack is enabled in WPF applications.</span></span> <span data-ttu-id="75959-209">자세한 내용은 참조 [완화: 포인터 기반 터치 및 스타일러스 지원](Mitigation:%20Pointer-based%20Touch%20and%20Stylus%20Support.md)</span><span class="sxs-lookup"><span data-stu-id="75959-209">For more information, see [Mitigation: Pointer-based Touch and Stylus Support](Mitigation:%20Pointer-based%20Touch%20and%20Stylus%20Support.md)</span></span> | 
|`Switch.System.Windows.Media.ImageSourceConverter`<br/>`OverrideExceptionWithNullReferenceException`|<span data-ttu-id="75959-210">레거시 있는지 여부를 제어 [NullReferenceException](xref:System.NullReferenceException) 대신 예외의 원인을 더 구체적으로 나타내는 예외가 throw 됩니다 (같은 [DirectoryNotFoundException](xref:System.IO.DirectoryNotFoundException) 또는 [ FileNotFoundException](xref:System.IO.FileNotFoundException)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-210">Controls whether a legacy [NullReferenceException](xref:System.NullReferenceException) is thrown instead of the exception that more specifically indicates the cause of the exception (such as a [DirectoryNotFoundException](xref:System.IO.DirectoryNotFoundException) or a [FileNotFoundException](xref:System.IO.FileNotFoundException).</span></span> <span data-ttu-id="75959-211">처리에 의존 하는 코드에서 사용 하기 위해 용도가 [NullReferenceException](xref:System.NullReferenceException)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-211">It is intended for use by code that depends on handling the [NullReferenceException](xref:System.NullReferenceException).</span></span> | <span data-ttu-id="75959-212">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="75959-212">.NET Framework 4.7</span></span> |
|`System.Xml.`<br /><br /> `IgnoreEmptyKeySequences`|<span data-ttu-id="75959-213">XSD 스키마 유효성 검사 하 여 복합 키에 빈 키 시퀀스가 무시 되는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-213">Controls whether empty key sequences in compound keys are ignored by XSD schema validation.</span></span> <span data-ttu-id="75959-214">자세한 내용은 참조 [완화: XML 스키마 유효성 검사](~/docs/framework/migration-guide/mitigation-xml-schema-validation.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-214">For more information, see [Mitigation: XML Schema Validation](~/docs/framework/migration-guide/mitigation-xml-schema-validation.md).</span></span>|<span data-ttu-id="75959-215">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="75959-215">.NET Framework 4.6</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="75959-216">추가 하는 대신는 `AppContextSwitchOverrides` 응용 프로그램 구성 파일에 요소를 설정할 수도 있습니다는 스위치 프로그래밍 방식으로 호출 하 여는 `static` (C#에서) 또는 `Shared` (Visual Basic)에서는 <xref:System.AppContext.SetSwitch%2A?displayProperty=nameWithType> 메서드.</span><span class="sxs-lookup"><span data-stu-id="75959-216">Instead of adding an `AppContextSwitchOverrides` element to an application configuration file, you can also set the switches programmatically by calling the `static` (in C#) or `Shared` (in Visual Basic) <xref:System.AppContext.SetSwitch%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="75959-217">라이브러리 개발자 라이브러리의 이후 버전에서 도입 되거나 변경 된 기능을 취소 하기 위해 호출자를 허용 하려면 사용자 지정 스위치 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75959-217">Library developers can also define custom switches to allow callers to opt out of changed functionality introduced  in later versions of their libraries.</span></span> <span data-ttu-id="75959-218">자세한 내용은 <xref:System.AppContext> 클래스를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75959-218">For more information, see the <xref:System.AppContext> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="75959-219">예제</span><span class="sxs-lookup"><span data-stu-id="75959-219">Example</span></span>  
 <span data-ttu-id="75959-220">다음 예제에서는 `AppContextSwitchOverrides` 단일 응용 프로그램 호환성 스위치를 정의 하는 요소 `Switch.System.Globalization.NoAsyncCurrentCulture`, 비동기 메서드 호출에 스레드를 넘어서 전달에서 culture에 맞지 않는 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-220">The following example uses the `AppContextSwitchOverrides` element to define a single application  compatibility switch, `Switch.System.Globalization.NoAsyncCurrentCulture`, that prevents culture from flowing across threads in asynchronous method calls.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <AppContextSwitchOverrides value="Switch.System.Globalization.NoAsyncCurrentCulture=true" />  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="75959-221">다음 예제에서는 `AppContextSwitchOverrides` 두 응용 프로그램 호환성 스위치를 정의 하는 요소 `Switch.System.Globalization.NoAsyncCurrentCulture` 및 `Switch.System.IO.BlockLongPaths`합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-221">The following example uses the `AppContextSwitchOverrides` element to define two application  compatibility switches, `Switch.System.Globalization.NoAsyncCurrentCulture` and `Switch.System.IO.BlockLongPaths`.</span></span> <span data-ttu-id="75959-222">Note 세미콜론 두 개의 이름/값 쌍을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="75959-222">Note that a semicolon separates the two name/value pairs.</span></span>  
  
```xml  
<configuration>  
    <runtime>  
       <AppContextSwitchOverrides   
          value="Switch.System.Globalization.NoAsyncCurrentCulture=true;Switch.System.IO.BlockLongPaths=true" />  
    </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="75959-223">참고 항목</span><span class="sxs-lookup"><span data-stu-id="75959-223">See Also</span></span>  
 [<span data-ttu-id="75959-224">AppContext</span><span class="sxs-lookup"><span data-stu-id="75959-224">AppContext</span></span>](xref:System.AppContext?qualifyHint=False&autoUpgrade=True)  
 [<span data-ttu-id="75959-225">\<런타임 > 요소</span><span class="sxs-lookup"><span data-stu-id="75959-225">\<runtime> Element</span></span>](runtime-element.md)  
 [<span data-ttu-id="75959-226">\<configuration> 요소</span><span class="sxs-lookup"><span data-stu-id="75959-226">\<configuration> Element</span></span>](../configuration-element.md)