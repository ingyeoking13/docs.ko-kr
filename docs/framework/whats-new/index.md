---
title: ".NET Framework의 새로운 기능 | Microsoft Docs"
ms.custom: 
ms.date: 05/02/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- what's new [.NET Framework]
ms.assetid: 1d971dd7-10fc-4692-8dac-30ca308fc0fa
caps.latest.revision: 292
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Human Translation
ms.sourcegitcommit: ddcefb2b35f8cbf06a3abcc16158eee850f799ff
ms.openlocfilehash: 3b6835c2e2c8ae590c642d5534cd1bae5645db6f
ms.contentlocale: ko-kr
ms.lasthandoff: 05/03/2017

---
# <a name="whats-new-in-the-net-framework"></a>.NET Framework의 새로운 기능
<a name="introduction"></a> 이 문서에서는 다음 버전의 .NET Framework에 새로 추가된 주요 기능과 향상된 내용에 대해 요약합니다.

 [.NET Framework 4.7](#v47) 
 [.NET Framework 4.6.2](#v462) 
 [.NET Framework 4.6.1](#v461) 
 [.NET 2015 및 .NET Framework 4.6](#v46) 
 [.NET Framework 4.5.2](#v452) 
 [.NET Framework 4.5.1](#v451) 
 [.NET Framework 4.5](#core)

 이 문서는 각 새로운 기능에 대한 포괄적인 정보를 제공하지 않으며 변경될 수 있습니다. .NET Framework에 대한 일반적인 내용은 [시작](../../../docs/framework/get-started/index.md)을 참조하십시오. 지원되는 플랫폼은 [시스템 요구 사항](~/docs/framework/get-started/system-requirements.md)을 참조하십시오. 다운로드 링크와 설치 지침은 [설치 가이드](../../../docs/framework/install/guide-for-developers.md)를 참조하십시오.

> [!NOTE]
>  .NET Framework 팀에서는 플랫폼 지원을 확장하고 새로운 기능(예: 변경할 수 없는 컬렉션 및 SIMD 사용 벡터 형식)을 도입하기 위한 NuGet이 있는 번외 기능도 릴리스했습니다. 자세한 내용은 [추가 클래스 라이브러리 및 API](../additional-apis/index.md) 및 [.NET Framework 및 번외 릴리스](~/docs/framework/get-started/the-net-framework-and-out-of-band-releases.md)를 참조하십시오. .NET Framework에 대해서는 [NuGet 패키지의 전체 목록](https://blogs.msdn.microsoft.com/dotnet/p/nugetpackages/)을 참조하거나 [피드](https://nuget.org/api/v2/curated-feeds/dotnetframework/Packages/)를 구독하십시오.

<a name="v47"></a> 
## <a name="introducing-the-net-framework-47"></a>.NET Framework 4.7 소개
 .NET Framework 4.7은 .NET Framework 4.6, 4.6.1 및 4.6.2에서 빌드되며 제품의 안정성을 유지하면서 많은 새로운 수정 및 여러 가지 새 기능이 추가됩니다.

### <a name="downloading-and-installing-the-net-framework-47"></a>.NET Framework 4.7 다운로드 및 설치
 
다음 위치에서 .NET Framework 4.7을 다운로드할 수 있습니다.

- [.NET Framework 4.7 웹 설치 관리자](http://go.microsoft.com/fwlink/?LinkId=825299)

- [.NET Framework 4.7 오프라인 설치 관리자](http://go.microsoft.com/fwlink/?LinkId=825303)

.NET Framework 4.7은 Windows 10, Windows 8.1, Windows 7 및 Windows Server 2008 R2 SP1 이상의 해당 서버 플랫폼에 설치할 수 있습니다. 웹 설치 관리자 또는 오프라인 설치 관리자를 사용하여 .NET Framework 4.7을 설치할 수 있습니다. 대부분의 사용자에게 권장되는 방법은 웹 설치 관리자를 사용하는 것입니다.

[.NET Framework 4.7 개발자 팩](http://go.microsoft.com/fwlink/?LinkId=825319)을 설치하여 Visual Studio 2012 이상 버전에서 .NET Framework 4.7을 대상으로 할 수 있습니다.

### <a name="whats-new-in-the-net-framework-47"></a>.NET Framework 4.7의 새로운 기능

.NET Framework 4.7에는 다음과 같은 영역의 새 기능이 포함됩니다.

- [핵심](#Core47)
- [네트워킹](#net47)
- [ASP.NET](#ASP-NET47)
- [WCF(Windows Communication Foundation)](#wcf47)
- [Windows Forms](#wf47)
- [WPF(Windows Presentation Foundation)](#WPF47)

.NET Framework 4.7에 추가된 새 API 목록은 GitHub에서 [.NET Framework 4.7 API 변경 내용](https://github.com/Microsoft/dotnet/blob/master/releases/net47/dotnet47-api-changes.md)을 참조하세요. .NET Framework 4.7의 향상된 기능 및 버그 수정 목록은 GitHub에서 [.NET Framework 4.7 변경 내용 목록](http://gutithub.com/Microsoft/dotnet/blob/master/releases/net47/dotnet47-changes.md)을 참조하세요.  자세한 내용은 .NET 블로그에서 [.NET Framework 4.7 알림](https://blogs.msdn.microsoft.com/dotnet/2017/04/05/announcing-the-net-framework-4-7/)을 참조하세요.

<a name="Core47" />
#### <a name="core"></a>핵심

.NET Framework 4.7에서는 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>를 통해 serialization이 향상됩니다.

**ECC(Elliptic Curve 암호화)로 향상된 기능***

.NET Framework 4.7에서는 개체가 이미 설정된 키를 나타낼 수 있도록 하기 위해 <xref:System.Security.Cryptography.ECDsa> 및 <xref:System.Security.Cryptography.ECDiffieHellman> 클래스에 `ImportParameters(ECParameters)` 메서드가 추가되었습니다. 또한 명시적 곡선 매개 변수를 사용하여 키를 내보내기 위한 `ExportParameters(Boolean)` 메서드도 추가되었습니다.

그뿐 아니라 .NET Framework 4.7에서는 추가 곡선(Brainpool 곡선 도구 모음 포함)에 대한 지원을 추가하며, 새로운 <xref:System.Security.Cryptography.ECDsa.Create%2A> 및 <xref:System.Security.Cryptography.ECDiffieHellman.Create%2A>팩터리 메서드를 통한 쉬운 생성을 위해 미리 정의된 정의도 추가적으로 제공합니다.

GitHub에서 [.NET Framework 4.7 암호화 개선 예제](https://gist.github.com/richlander/5a182899895a87a296c21ada97f7a54e)를 참조할 수 있습니다.

**DataContractJsonSerializer를 통한 보다 나은 제어 문자 지원**

.NET Framework 4.7에서 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>는 ECMAScript 6 표준에 따라 제어 문자를 serialize합니다. 이 동작은 .NET Framework 4.7을 대상으로 하는 응용 프로그램에 대해 기본적으로 사용되도록 설정되며, .NET Framework 4.7에서 실행되지만 이전 버전의 .NET Framework를 대상으로 하는 응용 프로그램에 대한 옵트인 기능입니다. 자세한 내용은 [.NET Framework 4.7의 대상 다시 지정 변경 내용](../../../docs/framework/migration-guide/retargeting-changes-in-the-net-framework-4-7.md)을 참조하세요.

<a name="net47" />
#### <a name="networking"></a>네트워킹

.NET Framework 4.7에서는 다음과 같은 네트워크 관련 기능을 추가합니다.

**TLS 프로토콜에 대 한 기본 운영 체제 지원***

<xref:System.Net.Security.SslStream?displayProperty=fullName> 및 업스택 구성 요소(예: HTTP, FTP, SMTP)에서 사용되는 TLS 스택을 통해 개발자들은 운영 체제에서 지원하는 기본 TLS 프로토콜을 사용할 수 있습니다. 개발자에게 더 이상 하드 코딩 TLS 버전은 필요하지 않습니다.

<a name="ASP-NET47" />
#### <a name="aspnet"></a>ASP.NET

NET Framework 4.7에서 ASP.NET에는 다음과 같은 새 기능이 포함됩니다.

**개체 캐시 확장성**

.NET Framework 4.7부터 ASP.NET에서는 개발자가 메모리 내 개체 캐싱 및 메모리 모니터링을 위한 기본 ASP.NET 구현을 대체할 수 있도록 하는 새로운 API 집합을 추가적으로 제공합니다. 개발자는 이제 ASP.NET 구현이 적절하지 않은 경우 다음 세 가지 구성 요소 중 하나를 바꿀 수 있습니다.

- **개체 캐시 저장소**. 개발자는 새 캐시 공급자 구성 섹션에서 새 **ICacheStoreProvider** 인터페이스를 사용하여 ASP.NET 응용 프로그램의 새로운 개체 캐시 구현을 연결할 수 있습니다.
 
- **메모리 모니터링**. ASP.NET의 기본 메모리 모니터는 프로세스에 대해 구성된 전용 바이트 제한에 가까워지거나 컴퓨터의 사용 가능한 총 실제 RAM이 부족할 때 응용 프로그램에 알립니다. 이러한 제한에 가까워지면 알림이 발생합니다. 일부 응용 프로그램의 경우 알림이 구성된 제한에 너무 가까운 상태에서 발생하여 제대로 대응하지 못하게 됩니다. 개발자는 이제 자체 메모리 모니터를 사용하여 <xref:System.Web.Hosting.ApplicationMonitors.MemoryMonitor%2A?displayProperty=fullName> 속성을 통해 기본값을 바꿀 수 있습니다.

- **메모리 제한 반응**. 기본적으로 ASP.NET은 전용 바이트 제한이 가까워질 경우 개체 캐시를 트리밍하고 주기적으로 <xref:System.GC.Collect%2A?displayProperty=fullName>를 호출합니다. 일부 응용 프로그램의 경우 <xref:System.GC.Collect%2A?displayProperty=fullName> 호출 빈도 또는 트리밍되는 개체 양이 효율적이지 않습니다. 이제 개발자는 **IObserver** 구현을 응용 프로그램의 메모리 모니터에 구독하여 기본 동작을 바꾸거나 보완할 수 있습니다.

<a name="wcf47" />
#### <a name="windows-communication-foundation-wcf"></a>WCF(Windows Communication Foundation)

WFC(Windows Communication Foundation)는 다음과 같은 기능 및 변경 내용을 추가합니다.

**TLS1.1.1 또는 TLS1.2에 대한 기본 메시지 보안 설정 구성 가능**

.NET Framework 4.7부터 WCF에서 SSL 3.0 및 TSL 1.0 외에도 TSL 1.1 또는 TLS 1.2를 기본 메시지 보안 프로토콜로 구성할 수 있습니다. 이것은 옵트인 설정으로 이 기능을 사용하려면 응용 프로그램 구성 파일에 다음 항목을 추가해야 합니다.

```xml
<runtime>
   <AppContextSwitchOverrides value="Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false" /> 
</runtime>
```

**WCF 응용 프로그램 및 WCF serialization의 향상된 안정성**

WCF에는 경합 상태를 제거하는 다양한 코드 변경 내용이 포함되어 있으므로 serialization 옵션의 성능과 안정성이 향상됩니다. 여기에는 다음이 포함됩니다.

- **SocketConnection.BeginRead** 및 **SocketConnection.Read** 호출에서 보다 향상된 비동기식 및 동기식 코드 혼합
- **SharedConnectionListener** 및 **DuplexChannelBinder**와의 연결 중단 시 안정성 향상
- <xref:System.Runtime.Serialization.FormatterServices.GetSerializableMembers%28System.Type%29?displayProperty=fullName> 메서드를 호출할 때 serialization 작업의 안정성 향상
- **ChannelSynchronizer.RemoveWaiter** 메서드를 호출하여 waiter를 제거할 때 안정성 개선

<a name="wf47" />
#### <a name="windows-forms"></a>Windows Forms

.NET Framework 4.7에서 Windows Forms는 높은 DPI 모니터에 대한 지원을 향상시킵니다.

**높은 DPI 지원**

.NET Framework 4.7을 대상으로 하는 응용 프로그램부터, .NET Framework는 Windows Forms 응용 프로그램에 대한 높은 DPI 및 동적 DPI 지원을 제공합니다. 높은 DPI 지원은 높은 DPI 모니터에는 폼 및 컨트롤의 모양과 레이아웃을 개선합니다. 동적 DPI는 사용자가 실행 중인 응용 프로그램의 DPI 또는 디스플레이 배율을 변경할 때 폼 및 컨트롤의 모양과 레이아웃을 변경합니다.

높은 DPI 지원은 응용 프로그램 구성 파일의 [\<System.Windows.Forms.ConfigurationSection>](../configure-apps/file-schema/winforms/index.md) 섹션을 정의하여 구성하는 옵트인 기능입니다. Windows Forms 응용 프로그램에 높은 DPI 지원 및 동적 DPI 지원을 추가하는 방법에 대한 자세한 내용은 [Windows Forms의 높은 DPI 지원](../winforms/high-dpi-support-in-windows-forms.md)을 참조하세요.

<a name="WPF47"></a> 
#### <a name="windows-presentation-foundation-wpf"></a>WPF(Windows Presentation Foundation)

.NET Framework 4.7의 WPF에는 다음과 같은 향상된 기능이 포함되어 있습니다.

**Windows WM_POINTER 메시지 기반의 터치/스타일러스 스택 지원**

WISP(Windows 잉크 서비스 플랫폼) 대신 [WM_POINTER 메시지](https://msdn.microsoft.com/library/windows/desktop/hh454903.aspx) 기반의 터치/스타일러스 스택 사용 옵션이 제공됩니다. 이것은 .NET Framework의 옵트인 기능입니다. 자세한 내용은 [.NET Framework 4.7의 대상 다시 지정 변경 내용](../migration-guide/retargeting-changes-in-the-net-framework-4-7.md)을 참조하세요.

**WPF 인쇄 API에 대한 새로운 구현**

<xref:System.Printing.PrintQueue?displayProperty=fullName> 클래스의 WPF 인쇄 API는 사용되지 않는 [XPS 인쇄 API](https://msdn.microsoft.com/library/windows/desktop/ff686814(v=vs.85).aspx) 대신, Windows [인쇄 문서 패키지 API](https://msdn.microsoft.com/library/windows/desktop/hh448418(v=vs.85).aspx)를 호출합니다. 이러한 변경 내용이 응용 프로그램 호환성에 미치는 영향에 대해서는 [.NET Framework 4.7의 대상 다시 지정 변경 내용](../migration-guide/retargeting-changes-in-the-net-framework-4-7.md)을 참조하세요. 

<a name="v462"></a> 
## <a name="whats-new-in-the-net-framework-462"></a>.NET Framework 4.6.2의 새로운 기능
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에는 다음과 같은 영역의 새 기능이 포함됩니다.

- [ASP.NET](#ASPNET462)

- [문자 범주](#Strings)

- [암호화](#Crypto462)

- [SqlClient](#SQLClient)

- [Windows Communication Foundation](#WCF)

- [WPF(Windows Presentation Foundation)](#WPF462)

- [Windows WF(Workflow Foundation)](#WF462)

- [ClickOnce](#ClickOnce)

- [Windows Forms 및 WPF 앱을 UWP 앱으로 변환](#UWPConvert)

- [디버깅 기능 향상](#Debug462)

.NET Framework 4.6.2에 추가된 새 API 목록은 GitHub에서 [.NET Framework 4.6.2 API 변경 내용](https://github.com/Microsoft/dotnet/blob/master/releases/net462/dotnet462-api-changes.md)을 참조하세요. .NET Framework 4.6.2의 향상된 기능 및 버그 수정 목록은 GitHub에서 [.NET Framework 4.6.2 변경 내용 목록](http://go.microsoft.com/fwlink/?LinkId=708778)을 참조하세요.  자세한 내용은 .NET 블로그에서 [.NET Framework 4.6.2 알림](https://blogs.msdn.microsoft.com/dotnet/2016/08/02/announcing-net-framework-4-6-2/)을 참조하십시오.

<a name="ASPNET462"></a> 
### <a name="aspnet"></a>ASP.NET
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]의 ASP.NET에는 다음과 같은 향상된 기능이 포함되어 있습니다.

 **데이터 주석 유효성 검사기의 지역화된 오류 메시지에 대한 지원 향상** 
 데이터 주석 유효성 검사기를 통해 클래스 속성에 하나 이상의 특성을 추가하여 유효성 검사를 수행할 수 있습니다. 유효성 검사에 실패하면 해당 특성의 <xref:System.ComponentModel.DataAnnotations.ValidationAttribute.ErrorMessage%2A?displayProperty=fullName> 요소가 오류 메시지 텍스트를 정의합니다. [!INCLUDE[net_v462](../../../includes/net-v462-md.md)] 이상에서는 ASP.NET을 사용하여 오류 메시지를 쉽게 지역화할 수 있습니다. 다음과 같은 경우에 오류 메시지를 지역화합니다.

1.  <xref:System.ComponentModel.DataAnnotations.ValidationAttribute.ErrorMessage%2A?displayProperty=fullName>가 유효성 검사 특성에 제공되는 경우

2.  리소스 파일 App_LocalResources 폴더에 저장되어 있는 경우

3.  지역화된 리소스 파일의 이름이 `DataAnnotation.Localization.{`*이름*`}.resx` 형식인 경우(여기서 *이름*은 *languageCode*`-`*country/regionCode* 또는 *languageCode* 형식의 문화권 이름임)

4.  리소스의 키 이름이 <xref:System.ComponentModel.DataAnnotations.ValidationAttribute.ErrorMessage%2A?displayProperty=fullName> 특성에 할당된 문자열이며 그 값이 지역화된 오류 메시지인 경우

 예를 들어, 다음 데이터 주석 특성은 잘못된 등급에 대한 기본 문화권의 오류 메시지를 정의합니다.

```csharp
public class RatingInfo
{
   [Required(ErrorMessage = "The rating must be between 1 and 10.")]
   [Display(Name = "Your Rating")]
   public int Rating { get; set; }
}
```

```vb
Public Class RatingInfo
   <Required(ErrorMessage = "The rating must be between 1 and 10.")>
   <Display(Name = "Your Rating")>
   Public Property Rating As Integer = 1
End Class
```

 그런 다음 키가 오류 메시지 문자열이고 값이 지역화된 오류 메시지인 리소스 파일 DataAnnotation.Localization.fr.resx를 만들 수 있습니다. 해당 파일은 `App.LocalResources` 폴더에서 찾아야 합니다. 예를 들면, 다음은 지역화된 프랑스어(fr) 오류 메시지의 값과 키입니다.

|이름|값|
|----------|-----------|
|등급은 1에서 10 사이여야 합니다.|La note doit être comprise entre 1 et 10.|

 그러면 이 파일은 다음을 할 수 있습니다.

 또한, 데이터 주석 지역화를 확장할 수 있습니다. 개발자는 <xref:System.Web.Globalization.IStringLocalizerProvider> 인터페이스를 구현하여 리소스 파일 내부 이외의 위치에 지역화 문자열을 저장함으로써 문자열 로컬라이저 공급자를 연결할 수 있습니다.

 **세션 상태 저장소 공급자와 비동기 지원**
 이제 ASP.NET을 통해 태스크 반환 메서드를 세션 상태 저장소 공급자와 함께 사용할 수 있으므로, ASP.NET 앱에서 비동기화의 확장성 이점을 누릴 수 있습니다. 세션 상태 저장소 공급자와의 비동기 작업을 지원하기 위해 ASP.NET에는 <xref:System.Web.SessionState.ISessionStateModule?displayProperty=fullName>이라는 새 인터페이스가 포함되어 있으며 이를 통해 개발자가 자체 세션 상태 모듈과 비동기 세션 저장소 공급자를 구현할 수 있습니다. 인터페이스는 다음과 같이 정의됩니다.

```csharp

public interface ISessionStateModule : IHttpModule {
    void ReleaseSessionState(HttpContext context);
    Task ReleaseSessionStateAsync(HttpContext context);
}

```

 또한 <xref:System.Web.SessionState.SessionStateUtility> 클래스에는 비동기 작업을 지원하는 데 사용할 수 있는 두 가지 새로운 메서드 <xref:System.Web.SessionState.SessionStateUtility.IsSessionStateReadOnly%2A> 및 <xref:System.Web.SessionState.SessionStateUtility.IsSessionStateRequired%2A>가 포함되어 있습니다.

 **출력 캐시 공급자에 대한 비동기 지원**
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)] 이상에서는 태스크 반환 메서드를 출력 캐시 공급자와 함께 사용하여 비동기화의 확장성 이점을 제공할 수 있습니다.  이러한 메서드를 구현하는 공급자는 웹 서버에서 스레드 차단을 줄이고 ASP.NET 서비스의 확장성을 개선합니다.

 비동기 출력 캐시 공급자를 지원하기 위해 다음 API를 추가했습니다.

- <xref:System.Web.Caching.OutputCacheProviderAsync?displayProperty=fullName> 클래스는 <xref:System.Web.Caching.OutputCacheProvider?displayProperty=fullName>에서 상속되며 이를 통해 개발자가 비동기 출력 캐시 공급자를 구현할 수 있습니다.

- <xref:System.Web.Caching.OutputCacheUtility> 클래스는 출력 캐시를 구성하기 위한 도우미 메서드를 제공합니다.

- <xref:System.Web.HttpCachePolicy?displayProperty=fullName> 클래스에 18개의 새 메서드가 있습니다. 여기에 <xref:System.Web.HttpCachePolicy.GetCacheability%2A>, <xref:System.Web.HttpCachePolicy.GetCacheExtensions%2A>, <xref:System.Web.HttpCachePolicy.GetETag%2A>, <xref:System.Web.HttpCachePolicy.GetETagFromFileDependencies%2A>, <xref:System.Web.HttpCachePolicy.GetMaxAge%2A>, <xref:System.Web.HttpCachePolicy.GetMaxAge%2A>, <xref:System.Web.HttpCachePolicy.GetNoStore%2A>, <xref:System.Web.HttpCachePolicy.GetNoTransforms%2A>, <xref:System.Web.HttpCachePolicy.GetOmitVaryStar%2A>, <xref:System.Web.HttpCachePolicy.GetProxyMaxAge%2A>, <xref:System.Web.HttpCachePolicy.GetRevalidation%2A>, <xref:System.Web.HttpCachePolicy.GetUtcLastModified%2A>, <xref:System.Web.HttpCachePolicy.GetVaryByCustom%2A>, <xref:System.Web.HttpCachePolicy.HasSlidingExpiration%2A> 및 <xref:System.Web.HttpCachePolicy.IsValidUntilExpires%2A>가 포함됩니다.

- <xref:System.Web.HttpCacheVaryByContentEncodings?displayProperty=fullName> 클래스에 2개의 새 매서드 <xref:System.Web.HttpCacheVaryByContentEncodings.GetContentEncodings%2A> 및 <xref:System.Web.HttpCacheVaryByContentEncodings.SetContentEncodings%2A>가 있습니다.

- <xref:System.Web.HttpCacheVaryByHeaders?displayProperty=fullName> 클래스에 2개의 새 매서드 <xref:System.Web.HttpCacheVaryByHeaders.GetHeaders%2A> 및 <xref:System.Web.HttpCacheVaryByHeaders.SetHeaders%2A>가 있습니다.

- <xref:System.Web.HttpCacheVaryByParams?displayProperty=fullName> 클래스에 2개의 새 매서드 <xref:System.Web.HttpCacheVaryByParams.GetParams%2A> 및 <xref:System.Web.HttpCacheVaryByParams.SetParams%2A>가 있습니다.

- <xref:System.Web.Caching.AggregateCacheDependency?displayProperty=fullName> 클래스에 <xref:System.Web.Caching.AggregateCacheDependency.GetFileDependencies%2A> 메서드가 있습니다.

- <xref:System.Web.Caching.CacheDependency>에 <xref:System.Web.Caching.CacheDependency.GetFileDependencies%2A> 메서드가 있습니다.

<a name="Strings"></a> 
### <a name="character-categories"></a>문자 범주
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]의 문자는 [유니코드 표준 버전 8.0.0](http://www.unicode.org/versions/Unicode8.0.0/)을 기반으로 분류됩니다. [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] 및 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]의 문자는 유니코드 6.3 문자 범주를 기반으로 분류됩니다.

 유니코드 8.0 지원은 <xref:System.Globalization.CharUnicodeInfo> 클래스에 의한 문자 분류와 해당 클래스를 사용하는 유형 및 메서드로 제한됩니다. 여기에는 <xref:System.Globalization.StringInfo>클래스, 오버로드된 <xref:System.Char.GetUnicodeCategory%2A?displayProperty=fullName> 메서드 및 .NET Framework 정규식 엔진에서 인식되는 [문자 클래스](../../../docs/standard/base-types/character-classes-in-regular-expressions.md)가 포함됩니다.  문자 및 문자열 비교와 정렬은 이 변경의 영향을 받지 않으며, 기본 운영 체제, Windows 7 시스템 또는 .NET Framework에서 제공하는 문자 데이터를 계속해서 사용합니다.

 문자 범주를 유니코드 6.0에서 유니코드 7.0으로 변경하려면 유니코드 컨소시엄 웹 사이트에서 [유니코드 표준, 버전 7.0.0](http://www.unicode.org/versions/Unicode7.0.0/)을 참조하십시오. 유니코드 7.0에서 유니코드 8.0으로 변경하려면 유니코드 컨소시엄 웹 사이트에서 [유니코드 표준, 버전 8.0.0](http://www.unicode.org/versions/Unicode8.0.0/)을 참조하십시오.

<a name="Crypto462"></a> 
### <a name="cryptography"></a>암호화
 **FIPS 186-3 DSA를 포함하는 X509 인증서에 대한 지원** 
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서는 키가 FIPS 186-2 1024비트 제한을 초과하는 DSA(디지털 서명 알고리즘) X509 인증서에 대한 지원을 추가했습니다.

 FIPS 186-3의 더 큰 키 크기를 지원할 뿐만 아니라 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서는 SHA-2 해시 알고리즘 패밀리(SHA256, SHA384 및 SHA512)를 통한 컴퓨팅 시그니처를 허용합니다. FIPS 186 3 지원은 새로운 <xref:System.Security.Cryptography.DSACng?displayProperty=fullName> 클래스에서 지원됩니다.

 .NET Framework 4.6의 <xref:System.Security.Cryptography.RSA> 클래스 및 .NET Framework 4.6.1의 <xref:System.Security.Cryptography.ECDsa> 클래스에 대한 최신 변경에 따라 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]의 <xref:System.Security.Cryptography.DSA> 추상 기본 클래스에는 호출자가 캐스팅하지 않고 이 기능을 사용할 수 있도록 해주는 추가 메서드가 있습니다. 다음 예제와 같이 <xref:System.Security.Cryptography.X509Certificates.DSACertificateExtensions.GetDSAPrivateKey%2A?displayProperty=fullName> 확장 메서드를 호출하여 데이터에 서명할 수 있습니다.

```csharp
public static byte[] SignDataDsaSha384(byte[] data, X509Certificate2 cert)
{
    using (DSA dsa = cert.GetDSAPrivateKey())
    {
        return dsa.SignData(data, HashAlgorithmName.SHA384);
    }
}
```

```vb 
Public Shared Function SignDataDsaSha384(data As Byte(), cert As X509Certificate2) As Byte()
    Using DSA As DSA = cert.GetDSAPrivateKey()
        Return DSA.SignData(data, HashAlgorithmName.SHA384)
    End Using
End Function
```

 또한 다음 예제와 같이 <xref:System.Security.Cryptography.X509Certificates.DSACertificateExtensions.GetDSAPublicKey%2A?displayProperty=fullName> 확장 메서드를 호출하여 서명된 데이터를 확인할 수 있습니다.

```csharp
public static bool VerifyDataDsaSha384(byte[] data, byte[] signature, X509Certificate2 cert)
{
    using (DSA dsa = cert.GetDSAPublicKey())
    {
        return dsa.VerifyData(data, signature, HashAlgorithmName.SHA384);
    }
}
```

```vb
 Public Shared Function VerifyDataDsaSha384(data As Byte(), signature As Byte(), cert As X509Certificate2) As Boolean
    Using dsa As DSA = cert.GetDSAPublicKey()
        Return dsa.VerifyData(data, signature, HashAlgorithmName.SHA384)
    End Using
End Function
```

 **ECDiffieHellman 키 파생 루틴에 대한 입력 정확성 향상**
 .NET Framework 3.5에서는 세 가지 KDF(키 파생 함수) 루틴을 가진 타원 곡선 Diffie-Hellman 키 계약에 대한 지원을 추가했습니다. 루틴에 대한 입력과 루틴 자체는 <xref:System.Security.Cryptography.ECDiffieHellmanCng> 개체에 대한 속성을 통해 구성했습니다. 하지만 일부 루틴이 일부 입력 속성을 읽지 않기 때문에 개발자의 과거에 대해 혼동을 일으킬 여지가 충분합니다.

 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 이 문제를 해결하기 위해 이러한 KDF 루틴과 해당 입력을 보다 정확하게 표시하도록 다음 세 가지 메서드를 <xref:System.Security.Cryptography.ECDiffieHellman> 기본 클래스에 추가했습니다.

|ECDiffieHellman 메서드|설명|
|----------------------------|-----------------|
|<xref:System.Security.Cryptography.ECDiffieHellman.DeriveKeyFromHash%28System.Security.Cryptography.ECDiffieHellmanPublicKey%2CSystem.Security.Cryptography.HashAlgorithmName%2CSystem.Byte%5B%5D%2CSystem.Byte%5B%5D%29>|수식을 사용하여 키 자료 파생<br /><br /> HASH(secretPrepend &#124;&#124; *x* &#124;&#124; secretAppend)<br /><br /> HASH(secretPrepend OrElse *x* OrElse secretAppend)<br /><br /> 여기서 *x*는 EC Diffie-hellman 알고리즘의 계산된 결과입니다.|
|<xref:System.Security.Cryptography.ECDiffieHellman.DeriveKeyFromHmac%28System.Security.Cryptography.ECDiffieHellmanPublicKey%2CSystem.Security.Cryptography.HashAlgorithmName%2CSystem.Byte%5B%5D%2CSystem.Byte%5B%5D%2CSystem.Byte%5B%5D%29>|수식을 사용하여 키 자료 파생<br /><br /> HMAC(hmacKey, secretPrepend &#124;&#124; *x* &#124;&#124; secretAppend)<br /><br /> HMAC(hmacKey, secretPrepend OrElse *x* OrElse secretAppend)<br /><br /> 여기서 *x*는 EC Diffie-hellman 알고리즘의 계산된 결과입니다.|
|<xref:System.Security.Cryptography.ECDiffieHellman.DeriveKeyTls%28System.Security.Cryptography.ECDiffieHellmanPublicKey%2CSystem.Byte%5B%5D%2CSystem.Byte%5B%5D%29>|TLS PRF(의사 난수 함수) 파생 알고리즘을 사용하여 키 자료 파생|

 **지속형 키 대칭 암호화 지원**
 Windows 암호화 라이브러리(CNG)에서는 지속형 대칭 키 저장과 하드웨어에 저장된 대칭 키 사용에 대한 지원을 추가했습니다. 개발자는 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]를 통해 이 기능을 활용할 수 있습니다.  키 이름과 키 공급자가 구현별로 다르게 표시되므로, 이 기능을 사용하려면 기본 팩토리 접근 방식 대신 구체적인 구현 형식의 생성자를 활용해야 합니다(예: `Aes.Create` 호출).

 지속형 키 대칭 암호화 지원은 AES (<xref:System.Security.Cryptography.AesCng>) 및 3DES (<xref:System.Security.Cryptography.TripleDESCng>) 알고리즘을 위해 존재합니다. 예를 들면 다음과 같습니다.

```csharp
public static byte[] EncryptDataWithPersistedKey(byte[] data, byte[] iv)
{
    using (Aes aes = new AesCng("AesDemoKey", CngProvider.MicrosoftSoftwareKeyStorageProvider))
    {
        aes.IV = iv;

        // Using the zero-argument overload is required to make use of the persisted key
        using (ICryptoTransform encryptor = aes.CreateEncryptor())
        {
            if (!encryptor.CanTransformMultipleBlocks)
            {
                throw new InvalidOperationException("This is a sample, this case wasn’t handled...");
            }

            return encryptor.TransformFinalBlock(data, 0, data.Length);
        }
    }
}
```

```vb 
Public Shared Function EncryptDataWithPersistedKey(data As Byte(), iv As Byte()) As Byte()
    Using Aes As Aes = New AesCng("AesDemoKey", CngProvider.MicrosoftSoftwareKeyStorageProvider)
        Aes.IV = iv

        ' Using the zero-argument overload Is required to make use of the persisted key
        Using encryptor As ICryptoTransform = Aes.CreateEncryptor()
            If Not encryptor.CanTransformMultipleBlocks Then
                Throw New InvalidOperationException("This is a sample, this case wasn’t handled...")
            End If
            Return encryptor.TransformFinalBlock(data, 0, data.Length)
        End Using
    End Using
End Function
```

 **SHA-2 해시에 대한 SignedXml 지원**
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서는 RSA-SHA256, RSA-SHA384 및 RSA-SHA512 PKCS#1 시그니처 메서드, SHA256, SHA384 및 SHA512 참조 다이제스트 알고리즘에 대한 <xref:System.Security.Cryptography.Xml.SignedXml> 클래스에 지원을 추가했습니다.

 URI 상수는 <xref:System.Security.Cryptography.Xml.SignedXml>에 다음과 같이 모두 표시됩니다.

|SignedXml 필드|상수|
|---------------------|--------------|
|<xref:System.Security.Cryptography.Xml.SignedXml.XmlDsigSHA256Url>|"http://www.w3.org/2001/04/xmlenc#sha256"|
|<xref:System.Security.Cryptography.Xml.SignedXml.XmlDsigRSASHA256Url>|"http://www.w3.org/2001/04/xmldsig-more#rsa-sha256"|
|<xref:System.Security.Cryptography.Xml.SignedXml.XmlDsigSHA384Url>|"http://www.w3.org/2001/04/xmldsig-more#sha384"|
|<xref:System.Security.Cryptography.Xml.SignedXml.XmlDsigRSASHA384Url>|"http://www.w3.org/2001/04/xmldsig-more#rsa-sha384"|
|<xref:System.Security.Cryptography.Xml.SignedXml.XmlDsigSHA512Url>|"http://www.w3.org/2001/04/xmlenc#sha512"|
|<xref:System.Security.Cryptography.Xml.SignedXml.XmlDsigRSASHA512Url>|"http://www.w3.org/2001/04/xmldsig-more#rsa-sha512"|

 이러한 알고리즘에 대한 지원을 추가하기 위해 <xref:System.Security.Cryptography.CryptoConfig>에 사용자 지정 <xref:System.Security.Cryptography.SignatureDescription> 핸들러를 등록한 모든 프로그램은 이전과 마찬가지로 계속 기능하지만 현재는 플랫폼 기본값이 있으므로 <xref:System.Security.Cryptography.CryptoConfig> 등록이 더 이상 필요하지 않습니다.

<a name="SQLClient"></a> 
### <a name="sqlclient"></a>SqlClient
 SQL Server용 .NET Framework 데이터 공급자(<xref:System.Data.SqlClient?displayProperty=fullName>)는 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에 다음과 같은 새로운 기능을 포함합니다.

 **Azure SQL Database와의 연결 풀링 및 시간 초과**
 연결 풀링을 사용하도록 설정한 상태에서 시간 초과 또는 다른 오류가 발생할 경우 예외가 캐시되고 다음에 연결하려고 시도할 때 캐시된 예외가 5초~1분 동안 throw됩니다.  자세한 내용은 [SQL Server 연결 풀링(ADO.NET)](../../../docs/framework/data/adonet/sql-server-connection-pooling.md)을 참조하십시오.

 Azure SQL Database에 연결할 때 일반적으로 빠르게 복구되는 일시적인 오류로 인해 연결 시도가 실패할 수 있으므로 이 동작은 바람직하지 않습니다. 연결 재시도 경험을 효율적으로 최적화하기 위해 Azure SQL Database 연결이 실패할 때 연결 풀 차단 기간 동작을 제거합니다.

 새로운 `PoolBlockingPeriod` 키워드를 추가하여 앱에 가장 적합한 차단 기간을 선택할 수 있습니다. 값은 다음과 같습니다.

 `Auto`
 Azure SQL Database에 연결하는 응용 프로그램에 대한 연결 풀 차단 기간은 비활성화되고, 다른 SQL Server 인스턴스에 연결하는 응용 프로그램에 대한 연결 풀 차단 기간은 활성화됩니다. 기본값입니다. 서버 끝점 이름이 다음 중 하나로 끝나는 경우 Azure SQL Database로 간주됩니다.

- .database.windows.net

- .database.chinacloudapi.cn

- .database.usgovcloudapi.net

- .database.cloudapi.de

 `AlwaysBlock` 연결 풀 차단 기간이 항상 활성화됩니다.

 `NeverBlock` 연결 풀 차단 기간이 항상 비활성화됩니다.

 **Always Encrypted 기능 향상** SQLClient에서는 Always Encrypted에 대한 두 가지 향상된 기능을 도입했습니다.

- 암호화된 데이터베이스 열에 대한 매개 변수화된 쿼리 성능을 향상하기 위해 이제 쿼리 매개 변수에 대한 암호화 메타데이터가 캐시됩니다. <xref:System.Data.SqlClient.SqlConnection.ColumnEncryptionQueryMetadataCacheEnabled%2A?displayProperty=fullName> 속성을 `true`(기본값)로 설정 시 동일한 쿼리가 여러 번 호출되는 경우 클라이언트가 서버에서 한 번만 매개 변수 메타데이터를 검색합니다.

- 키 캐시의 열 암호화 키 항목은 이제 구성 가능한 시간 간격 후에 제거되며 <xref:System.Data.SqlClient.SqlConnection.ColumnEncryptionKeyCacheTtl%2A?displayProperty=fullName> 속성을 사용하여 설정됩니다.

<a name="WCF"></a> 
### <a name="windows-communication-foundation"></a>Windows Communication Foundation
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 Windows Communication Foundation이 다음과 같은 영역에서 향상되었습니다.

 **WCF 전송 보안에서 CNG를 사용하여 저장한 인증서 지원**
 WCF 전송 보안에서 Windows 암호화 라이브러리(CNG)를 사용하여 저장한 인증서를 지원합니다. [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 이 지원은 지수 길이가 32비트 이하인 공개 키로 인증서를 사용하도록 제한됩니다. 응용 프로그램이 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]를 대상으로 하는 경우 이 기능은 기본적으로 켜집니다.

 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] 및 이전 버전을 대상으로 하지만 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 실행 중인 응용 프로그램의 경우 app.config 또는 web.config 파일의 [\<runtime>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 섹션에 다음 줄을 추가하여 이 기능을 사용하도록 설정할 수 있습니다.

```xml
<AppContextSwitchOverrides
    value="Switch.System.ServiceModel.DisableCngCertificates=false"
/>
```

다음과 같은 코드를 사용하여 프로그래밍 방식으로 이 작업을 수행할 수도 있습니다.

```csharp
private const string DisableCngCertificates = @"Switch.System.ServiceModel.DisableCngCertificates";
AppContext.SetSwitch(disableCngCertificates, false);
```

```vb
Const DisableCngCertificates As String = "Switch.System.ServiceModel.DisableCngCertificates"
AppContext.SetSwitch(disableCngCertificates, False)
```

 **DataContractJsonSerializer 클래스에 의한 여러 일광 절약 시간 조정 규칙에 대한 지원 향상**
 고객이 응용 프로그램 구성 설정을 사용하여 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 클래스에서 단일 표준 시간대에 대해 여러 조정 규칙을 지원할지 여부를 결정할 수 있습니다. 이 기능은 옵트인(opt-in) 기능입니다. 이 기능을 사용하려면 app.config 파일에 다음 설정을 추가합니다.

```xml
<runtime>
     <AppContextSwitchOverrides value="Switch.System.Runtime.Serialization.DoNotUseTimeZoneInfo=false" />
</runtime>
```

이 기능을 사용하는 경우 날짜 및 시간 데이터를 역직렬화하기 위해 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 개체가 <xref:System.TimeZone> 형식 대신 <xref:System.TimeZoneInfo> 형식을 사용합니다. <xref:System.TimeZoneInfo>에서는 여러 조정 규칙을 지원하므로 기록 표준 시간대 데이터로 작업할 수 있지만 <xref:System.TimeZone>에서는 그렇지 않습니다.

<xref:System.TimeZoneInfo>구조 및 시간대 조정에 대한 자세한 내용은 [표준 시간대 개요](../../../docs/standard/datetime/time-zone-overview.md)를 참조하십시오.

**XMLSerializer 클래스로 serialize 및 deserialize할 때 UTC 시간 유지 지원** 일반적으로 <xref:System.Xml.Serialization.XmlSerializer> 클래스는 UTC <xref:System.DateTime> 값을 serialize하는 데 사용될 경우 날짜 및 시간을 유지하는 serialize된 시간 문자열을 만들지만 로컬 시간으로 간주됩니다.  예를 들어 다음 코드를 호출하여 UTC 날짜 및 시간을 인스턴스화하는 경우

```csharp
DateTime utc = new DateTime(2016, 11, 07, 3, 0, 0, DateTimeKind.Utc);
```

```vb
Dim utc As New Date(2016, 11, 07, 3, 0, 0, DateTimeKind.Utc)
```

UTC보다 8시간 늦은 시스템에 관해 serialize된 시간 문자열 "03:00:00.0000000-08:00"이 결과로 제공됩니다.  serialize된 값은 항상 로컬 날짜 및 시간 값으로 deserialize됩니다.

 응용 프로그램 구성 설정을 사용하여 <xref:System.DateTime> 값을 직렬화 및 역직렬화할 때 <xref:System.Xml.Serialization.XmlSerializer>에서 UTC 표준 시간대 정보를 유지할지 여부를 결정할 수 있습니다.

```xml 
<runtime>
     <AppContextSwitchOverrides 
          value="Switch.System.Runtime.Serialization.DisableSerializeUTCDateTimeToTimeAndDeserializeUTCTimeToUTCDateTime=false" />
</runtime>
```

이 기능을 사용하는 경우 날짜 및 시간 데이터를 역직렬화하기 위해 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 개체가 <xref:System.TimeZone> 형식 대신 <xref:System.TimeZoneInfo> 형식을 사용합니다. <xref:System.TimeZoneInfo>에서는 여러 조정 규칙을 지원하므로 기록 표준 시간대 데이터로 작업할 수 있지만 <xref:System.TimeZone>에서는 그렇지 않습니다.

<xref:System.TimeZoneInfo>구조 및 시간대 조정에 대한 자세한 내용은 [표준 시간대 개요](../../../docs/standard/datetime/time-zone-overview.md)를 참조하십시오.

 **NetNamedPipeBinding 가장 일치**
 WCF에는 클라이언트 응용 프로그램에서 요청한 항목과 가장 일치하는 URI를 수신하는 서비스에 항상 연결하도록 설정 가능한 새 앱 설정이 있습니다. 이 앱 설정을 `false`(기본값)로 지정한 경우 클라이언트에서 <xref:System.ServiceModel.NetNamedPipeBinding>을 사용하여 요청한 URI의 부분 문자열인 URI를 수신하는 서비스에 연결하려고 시도할 수 있습니다.

 예를 들어 클라이언트가 `net.pipe://localhost/Service1`에서 수신하는 서비스에 연결하려고 하지만, 관리자 권한으로 실행 중인 컴퓨터의 다른 서비스에서 `net.pipe://localhost`를 수신하고 있습니다. 이 앱 설정을 `false`로 지정한 경우 클라이언트에서 잘못된 서비스에 연결하려고 시도합니다. 앱 설정을 `true`로 설정하면 클라이언트에서는 항상 가장 일치하는 서비스에 연결합니다.

> [!NOTE]
>  <xref:System.ServiceModel.NetNamedPipeBinding>을 사용하는 클라이언트는 전체 끝점 주소 대신 서비스의 기준 주소(있는 경우)를 기반으로 서비스를 찾습니다. 이 설정을 항상 작동하게 하려면 서비스에서 고유 기준 주소를 사용해야 합니다.

 이 변경을 사용하려면 클라이언트 응용 프로그램의 App.config 또는 Web.config 파일에 다음 앱 설정을 추가합니다.

```xml
<configuration>
    <appSettings>
        <add key="wcf:useBestMatchNamedPipeUri" value="true" />
    </appSettings>
</configuration>
```

 **SSL 3.0은 기본 프로토콜이 아닙니다.**
 전송 보안 및 자격 증명 유형의 인증서를 지원하는 NetTcp를 사용할 경우 SSL 3.0은 더 이상 보안 연결을 협상하는 데 사용되는 기본 프로토콜이 아닙니다. 대부분의 경우 TLS 1.0이 NetTcp에 대한 프로토콜 목록에 포함되어 있으므로 기존 앱에는 영향을 주지 않습니다. 모든 기존 클라이언트에서는 TLS 1.0 이상을 사용하여 연결을 협상할 수 있습니다.      Ssl3가 필요한 경우 다음 구성 메커니즘 중 하나를 사용하여 협상된 프로토콜 목록에 Ssl3를 추가합니다.

- <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols%2A?displayProperty=fullName> 속성

- <xref:System.ServiceModel.TcpTransportSecurity.SslProtocols%2A?displayProperty=fullName> 속성

- [\<netTcpBinding>](../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md) 섹션의 [\<transport>](../../../docs/framework/configure-apps/file-schema/wcf/transport-of-nettcpbinding.md) 섹션

- [\<customBinding>](../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md) 섹션의 [\<sslStreamSecurity>](../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md) 섹션

<a name="WPF462"></a> 
### <a name="windows-presentation-foundation-wpf"></a>WPF(Windows Presentation Foundation)
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 Windows Presentation Foundation이 다음과 같은 영역에서 향상되었습니다.

 **그룹 정렬**
 <xref:System.Windows.Data.CollectionView> 개체를 사용하여 데이터를 그룹화하는 응용 프로그램에서는 이제 그룹 정렬 방법을 명시적으로 선언할 수 있습니다. 명시적으로 정렬하면 응용 프로그램에서 그룹을 동적으로 추가 또는 제거하거나 그룹화에 포함된 항목의 속성 값을 변경할 때 발생하는 직관적이지 않은 순서 지정 문제가 해결됩니다. 또한 그룹화 속성 비교를 전체 컬렉션 정렬에서 그룹화 정렬로 전환하여 그룹 만들기 프로세스의 성능을 향상할 수 있습니다.

 그룹 정렬을 지원하기 위해 새로운 <xref:System.ComponentModel.GroupDescription.SortDescriptions%2A?displayProperty=fullName> 및 <xref:System.ComponentModel.GroupDescription.CustomSort%2A?displayProperty=fullName> 속성을 통해 <xref:System.ComponentModel.GroupDescription> 개체에서 생성된 그룹 컬렉션을 정렬하는 방법이 기술됩니다. 이 방법은 동일하게 명명된 <xref:System.Windows.Data.ListCollectionView> 속성에서 데이터 항목을 정렬하는 방법을 설명하는 방식과 유사합니다.

 <xref:System.Windows.Data.PropertyGroupDescription> 클래스의 두 가지 새로운 정적 속성 <xref:System.Windows.Data.PropertyGroupDescription.CompareNameAscending%2A> 및 <xref:System.Windows.Data.PropertyGroupDescription.CompareNameDescending%2A>는 가장 일반적인 경우에 사용할 수 있습니다.

 예를 들어 다음 XAML은 데이터를 연령별로 그룹화하고, 연령 그룹을 오름차순으로 정렬한 다음 각 연령 그룹 내의 항목을 성별로 그룹화합니다.

```xaml
<GroupDescriptions>
     <PropertyGroupDescription 
         PropertyName=”Age” 
         CustomSort= 
              ”{x:Static PropertyGroupDescription.CompareNamesAscending}”/>
     </PropertyGroupDescription>
</GroupDescriptions>

<SortDescriptions>
     <SortDescription PropertyName=”LastName”/>
</SortDescriptions>
```

 **소프트 키보드 지원**
 소프트 키보드 지원을 사용하면 텍스트 입력을 수행할 수 있는 컨트롤을 통해 터치 입력을 수신할 때 Windows 10의 새로운 소프트 키보드를 자동으로 호출하거나 해제하여 WPF 응용 프로그램에서 포커스를 추적할 수 있습니다.

 이전 버전 .NET Framework의 WPF 응용 프로그램에서는 포커스 추적을 사용하려면 WPF 펜/터치 제스처 지원을 사용하지 않도록 설정해야 합니다.  따라서 WPF 응용 프로그램에서는 전체 WPF 터치 지원을 선택하거나 Windows 마우스 승격을 사용해야 합니다.

 **모니터별 DPI**
 WPF 앱에 대해 최근에 확산되는 높은 DPI 및 하이브리드 DPI 환경을 지원하기 위해 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]의 WPF에서는 모니터별 인식을 사용하도록 지정합니다. 모니터별 DPI를 인식하도록 WPF 앱을 설정하는 방법에 대한 자세한 내용은 GitHub의 [samples and developer guide](https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI)(샘플 및 개발자 가이드)를 참조하십시오.

 이전 버전의.NET Framework에서는 WPF 앱은 시스템 DPI를 인식합니다. 즉, 응용 프로그램의 UI는 앱이 렌더링되는 모니터의 DPI에 따라 OS에 의해 적절하게 확장됩니다. ,

 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)] 아래에서 실행 중인 앱의 경우 다음과 같이 응용 프로그램 구성 파일의 [\<runtime>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 섹션에 구성 문을 추가하여 WPF 앱에서 모니터별 DPI 변경을 사용하지 않도록 설정할 수 있습니다.

```xml
<runtime>
   <AppContextSwitchOverrides value=”Switch.System.Windows.DoNotScaleForDpiChanges=false”/>
</runtime>
```

<a name="WF462"></a> 
### <a name="windows-workflow-foundation-wf"></a>Windows WF(Workflow Foundation)
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 Windows Workflow Foundation이 다음과 같은 영역에서 향상되었습니다.

 **다시 호스트된 WF 디자이너에서 C# 식 및 IntelliSense 지원**
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 이상에서 WF는 Visual Studio 디자이너와 코드 워크플로 모두에서 C# 식을 지원합니다. 다시 호스트된 워크플로 디자이너는 Visual Studio 외부 응용 프로그램(예: WPF)에서 워크플로 디자이너가 위치할 수 있도록 해주는 WF의 주요 기능입니다.  Windows Workflow Foundation을 사용하면 다시 호스트된 워크플로 디자이너에서 C# 식 및 IntelliSense를 지원할 수 있습니다. 자세한 내용은 [Windows Workflow Foundation 블로그](http://go.microsoft.com/fwlink/?LinkID=809042&clcid=0x409)를 참조하십시오.

 `Availability of IntelliSense when a customer rebuilds a workflow project from Visual Studio`
 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)] 이전 버전의 .NET Framework에서는 고객이 Visual Studio에서 워크플로 프로젝트를 다시 작성할 때 WF Designer IntelliSense가 중단됩니다. 프로젝트가 빌드되면 워크플로 형식을 디자이너에서 찾을 수 없으므로 IntelliSense의 누락된 워크플로 형식에 대한 경고가 **오류 목록** 창에 표시됩니다. [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서는 이 문제를 해결하고 IntelliSense를 사용할 수 있도록 해줍니다.

 **워크플로 추적 기능이 설정된 Workflow V1 응용 프로그램을 이제 FIPS 모드로 실행 가능**
 이제 FIPS 규격 모드를 사용하는 컴퓨터에서 워크플로 추적이 설정된 워크플로 버전 1 스타일 응용 프로그램을 실행할 수 있습니다. 이 시나리오를 사용하려면 app.config 파일을 다음과 같이 변경해야 합니다.

```xml
<add key="microsoft:WorkflowRuntime:FIPSRequired" value="true" />
```

 이 시나리오를 사용하지 않도록 설정한 경우 응용 프로그램을 실행하면 계속해서 예외가 발생하고 “이 구현은 Windows Platform FIPS 유효성을 검사한 암호화 알고리즘의 일부가 아닙니다.”라는 메시지가 표시됩니다.

 **Visual Studio Workflow Designer에서 동적 업데이트를 사용할 때 워크플로 기능 향상**
 워크플로 디자이너, 순서도 활동 디자이너 및 기타 워크플로 활동 디자이너는 이제 <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.PrepareForUpdate%2A?displayProperty=fullName> 메서드를 호출한 이후에 저장된 워크플로를 로드하여 표시합니다. [!INCLUDE[net_v462](../../../includes/net-v462-md.md)] 이전의 .NET Framework 버전에서 <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.PrepareForUpdate%2A?displayProperty=fullName>를 호출한 후 저장된 워크플로에 대해 Visual Studio에 XAML 파일을 로드하면 다음과 같은 문제가 발생할 수 있습니다.

- 워크플로 디자이너가 XAML 파일을 올바르게 로드할 수 없습니다(<xref:System.Activities.Presentation.ViewState.ViewStateData.Id%2A?displayProperty=fullName>가 줄의 끝에 있는 경우).

- 순서도 활동 디자이너 또는 기타 워크플로 활동 디자이너는 연결된 속성 값과 달리 모든 개체를 기본 위치에 표시할 수 있습니다.

<a name="ClickOnce"></a> 
### <a name="clickonce"></a>ClickOnce
 ClickOnce는 이미 지원되는 1.0 프로토콜 외에 TLS 1.1 및 TLS 1.2를 지원하도록 업데이트되었습니다. ClickOnce는 필요한 프로토콜을 자동으로 검색하므로, TLS 1.1 및 1.2 지원하기 위해 ClickOnce 응용 프로그램에서 별도의 단계를 수행할 필요가 없습니다.

<a name="UWPConvert"></a> 
### <a name="converting-windows-forms-and-wpf-apps-to--uwp-apps"></a>Windows Forms 및 WPF 앱을 UWP 앱으로 변환
 이제 Windows에서는 기존 Windows 데스크톱 앱(예: WPF 및 Windows Forms 앱)을 UWP(유니버설 Windows 플랫폼)로 가져올 수 있습니다. 이 기술은 기존 코드 베이스를 UWP로 점차적으로 마이그레이션하여 앱을 모든 Windows 10 장치로 가져옴으로써 브리지 역할을 합니다.

 변환된 데스크톱 앱은 UWP 앱의 ID와 비슷한 앱 ID를 얻습니다. 이 ID를 사용하여 UWP API에 액세스하여 라이브 타일, 알림 등과 같은 기능을 사용할 수 있습니다. 앱은 이전과 동일하게 작동하고 완전히 신뢰할 수 있는 앱으로 실행됩니다. 앱이 변환되면 기존 완전 신뢰 프로세스에 앱 컨테이너 프로세스를 추가하여 적응형 사용자 인터페이스를 추가할 수 있습니다. 모든 기능을 앱 컨테이너 프로세스로 이동한 후 완전 신뢰 프로세스를 제거하고 모든 Windows 10 장치에서 새 UWP 앱을 사용할 수 있습니다.

<a name="Debug462"></a> 
### <a name="debugging-improvements"></a>디버깅 기능 향상
 단일 소스 코드 줄에서 `null`인 변수를 확인할 수 있도록 <xref:System.NullReferenceException>가 throw될 때 추가 분석을 수행하도록 [!INCLUDE[net_v462](../../../includes/net-v462-md.md)]에서 *관리되지 않는 디버깅 API*가 개선되었습니다.   이 시나리오를 지원하기 위해 관리되지 않는 디버깅 API에 다음 API를 추가했습니다.

- [ICorDebugCode4](../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md), [ICorDebugVariableHome](../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) 및 [ICorDebugVariableHomeEnum](../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md) 인터페이스: 관리되는 변수의 네이티브 홈을 노출합니다. 이렇게 하면 <xref:System.NullReferenceException>가 발생할 경우 디버거에서 일부 코드 흐름 분석을 수행하고 거꾸로 살펴보면서 네이티브 위치 `null`에 해당하는 관리되는 변수를 결정합니다.

- [ICorDebugType2::GetTypeID](../../../docs/framework/unmanaged-api/debugging/icordebugtype2-gettypeid-method.md) 메서드는 ICorDebugType을 [COR_TYPEID](../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)에 매핑하여 디버거가 ICorDebugType 인스턴스 없이 [COR_TYPEID](../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)를 가져올 수 있도록 해줍니다. 그런 다음 [COR_TYPEID](../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)의 기존 API를 사용하여 형식의 클래스 레이아웃을 결정할 수 있습니다.

<a name="v461"></a> 
## <a name="whats-new-in-the-net-framework-461"></a>.NET Framework 4.6.1의 새로운 기능
 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]에는 다음과 같은 영역의 새 기능이 포함됩니다.

- [암호화](#Crypto)

- [ADO.NET](#ADO.NET461)

- [WPF(Windows Presentation Foundation)](#WPF461)

- [Windows Workflow Foundation](#WWF461)

- [프로파일링](#Profile461)

- [NGen](#NGEN461)

 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]에 대한 자세한 내용은 다음 항목을 참조하세요.

- [.NET Framework 4.6.1 변경 내용 목록](http://go.microsoft.com/fwlink/?LinkId=622964)

- [4.6.1의 응용 프로그램 호환성](../../../docs/framework/migration-guide/application-compatibility-in-the-net-framework-4-6-1.md)

- [.NET Framework API 차이점](http://go.microsoft.com/fwlink/?LinkId=622989)(GitHub에서)

<a name="Crypto"></a> 
### <a name="cryptography-support-for-x509-certificates-containing-ecdsa"></a>암호화: ECDSA를 포함하는 X509 인증서 지원
 .NET Framework 4.6에는 x509 인증서를 위한 RSACng 지원이 추가되었습니다. [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]에는 ECDSA(타원 곡선 디지털 서명 알고리즘) X509 인증서에 대한 지원이 추가되었습니다.

 ECDSA는 RSA보다 더 향상된 성능과 더 안전한 암호화 알고리즘을 제공하므로 TLS(전송 계층 보안) 성능 및 확장성 면에서 최고의 선택이 될 것입니다. .NET Framework 구현은 기존 Windows 기능으로 호출을 래핑합니다.

 다음 예제 코드에서는 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]에 포함된 ECDSA  X509 인증서에 대한 새 지원을 사용하여 바이트 스트림을 위한 서명을 쉽게 생성하는 방법을 보여 줍니다.

 [!code-csharp[whatsnew.461.crypto#1](../../../samples/snippets/csharp/VS_Snippets_CLR/whatsnew.461.crypto/cs/Code46.cs#1)]
 [!code-vb[whatsnew.461.crypto#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/whatsnew.461.crypto/vb/Code461.vb#1)]

 다음은 .NET Framework 4.6에서 서명을 생성하는 데 필요한 코드에 표시된 대비를 제공합니다.

 [!code-csharp[whatsnew.461.crypto#2](../../../samples/snippets/csharp/VS_Snippets_CLR/whatsnew.461.crypto/cs/Code46.cs#2)]
 [!code-vb[whatsnew.461.crypto#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/whatsnew.461.crypto/vb/Code46.vb#2)]

<a name="ADO.NET461"></a> 
### <a name="adonet"></a>ADO.NET
 ADO.NET에는 다음이 추가되었습니다.

 하드웨어로 보호된 키에 대해 Always Encrypted 지원. ADO.NET은 이제 Always Encrypted 열 마스터 키를 기본적으로 HSM(하드웨어 보안 모듈)에 저장할 수 있습니다. 이 지원을 통해 고객은 사용자 지정 열 마스터 키 저장소 공급자를 작성하고 응용 프로그램에 등록하지 않고도 HSM에 저장된 비동기 키를 활용할 수 있습니다.

 HSM에 저장된 열 마스터 키로 보호된 상시 암호화 데이터에 액세스하려면 고객이 HSM 공급업체에서 제공한 CSP 공급자 또는 CNG 키 저장소 공급자를 앱 서버 또는 클라이언트 컴퓨터에 설치해야 합니다.

 AlwaysOn에 대해 <xref:System.Data.SqlClient.SqlConnectionStringBuilder.MultiSubnetFailover%2A> 연결 동작을 개선합니다. SqlClient는 이제 자동으로 AlwaysOn AG(가용성 그룹)에 대한 더 빠른 연결을 제공합니다. 응용 프로그램이 다른 서브넷의 AlwaysOn AG(가용성 그룹)에 연결되었는지 투명하게 감지하고 현재 활성 서버를 신속하게 검색하여 서버에 대한 연결을 제공합니다. 이 릴리스 전에는 AlwaysOn 가용성 그룹에 연결되었음을 나타내기 위해 응용 프로그램에서 `“MultisubnetFailover=true”`를 포함하도록 연결 문자열을 설정해야 했습니다. 연결 키워드를 `true`로 설정하지 않은 경우 응용 프로그램에서 AlwaysOn 가용성 그룹에 연결하는 동안 시간 초과가 발생할 수 있습니다. 이 릴리스를 통해 응용 프로그램에서 <xref:System.Data.SqlClient.SqlConnectionStringBuilder.MultiSubnetFailover%2A>을 `true`로 설정할 필요가 *없습니다*. Always On 가용성 그룹의 SqlClient 지원에 대한 자세한 내용은 [고가용성 및 재해 복구에 대한 SqlClient 지원](../../../docs/framework/data/adonet/sql/sqlclient-support-for-high-availability-disaster-recovery.md)을 참조하십시오.

<a name="WPF461"></a> 
### <a name="windows-presentation-foundation-wpf"></a>WPF(Windows Presentation Foundation)
 Windows Presentation Foundation에는 많은 향상된 기능 및 변경 내용이 포함되어 있습니다.

 성능 향상. [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]에서 터치 이벤트를 발생시킬 때의 지연이 수정되었습니다. 또한 빠른 입력 중 <xref:System.Windows.Controls.RichTextBox> 컨트롤에 입력한 내용이 더 이상 렌더링 스레드에 연결되지 않습니다.

 맞춤법 검사 향상. Windows 8.1 이상 버전에서는 추가 언어 맞춤법 검사에 대한 운영 체제 지원을 사용하도록 WPF의 맞춤법 검사기 기능이 업데이트되었습니다.  Windows 8.1 이전의 Windows 버전에 대해서는 기능이 변경되지 않았습니다.

 이전 버전의 .NET Framework와 마찬가지로, 다음 순서에 따라 정보를 검색하여 <xref:System.Windows.Controls.TextBox> 컨트롤 또는 <xref:System.Windows.Controls.RichTextBox> 블록의 언어를 감지합니다.

- `xml:lang`(있는 경우)

- 현재 입력 언어

- 현재 스레드 문화권

 WPF의 언어 지원에 대한 자세한 내용은 [.NET Framework 4.6.1 기능에 대한 WPF 블로그 게시물](http://go.microsoft.com/fwlink/?LinkID=691819)을 참조하십시오.

 사용자 단위 사용자 지정 사전에 대한 추가 지원. [!INCLUDE[net_v461](../../../includes/net-v461-md.md)]에서 WPF는 전역으로 등록된 사용자 지정 사전을 인식합니다. 컨트롤 단위로 등록하는 기능 외에 이 기능을 사용할 수 있습니다.

 WPF 이전 버전에서는 사용자 지정 사전에서 제외된 단어 및 자동 고침 목록을 인식하지 못했습니다. Windows 8.1 및 Windows 10에서는 `%AppData%\Microsoft\Spelling\<language tag>` 디렉터리에 저장할 수 있는 파일을 사용하여 이러한 기능이 지원됩니다.  이러한 파일에 적용되는 규칙은 다음과 같습니다.

- 파일의 확장명은 .dic(추가된 단어용), .exc(제외된 단어용) 또는 .acl(자동 고침용)입니다.

- 파일은 BOM(바이트 순서 표시)으로 시작하는 UTF-16 LE 일반 텍스트여야 합니다.

- 각 줄은 단어(추가되거나 제외된 단어 목록의 단어) 또는 단어가 세로 막대("&#124;")로 구분된 자동 고침 쌍(자동 고침 단어 목록)으로 구성되어야 합니다.

- 이러한 파일은 읽기 전용으로 간주되며 시스템에 의해 수정되지 않습니다.

> [!NOTE]
>  이러한 새 파일 형식은 WPF 맞춤법 검사 API에 의해 직접 지원되지 않으며 응용 프로그램에서 WPF에 제공된 사용자 지정 사전은 계속 .lex 파일을 사용해야 합니다.

 샘플. MSDN에는 많은 [WPF 샘플](https://msdn.microsoft.com/library/ms771633.aspx)이 있습니다. 가장 인기 있는 샘플(사용량에 따라) 200개 이상이 [오픈 소스 GitHub 리포지토리](https://github.com/Microsoft/WPF-Samples)로 이동될 예정입니다. 끌어오기 요청을 보내거나 [GitHub 문제](https://github.com/Microsoft/WPF-Samples/issues)를 열어 샘플 개선에 참여해 주세요.

 DirectX 확장. WPF에는 DX10 및 Dx11 콘텐츠와 쉽게 상호 운용할 수 있는 <xref:System.Windows.Interop.D3DImage>의 새 구현을 제공하는 [NuGet 패키지](http://go.microsoft.com/fwlink/?LinkID=691342)가 포함되어 있습니다. 이 패키지의 코드는 오픈 소스로 [GitHub](https://github.com/Microsoft/WPFDXInterop)에서 사용할 수 있습니다.

<a name="WWF461"></a> 
### <a name="windows-workflow-foundation-transactions"></a>Windows Workflow Foundation: 트랜잭션
 <xref:System.Transactions.Transaction.EnlistPromotableSinglePhase%2A?displayProperty=fullName> 메서드는 이제 MSDTC 이외의 분산 트랜잭션 관리자를 사용하여 트랜잭션을 승격할 수 있습니다. GUID 트랜잭션 프로모터 식별자를 새로운 <xref:System.Transactions.Transaction.EnlistPromotableSinglePhase%28System.Transactions.IPromotableSinglePhaseNotification%2CSystem.Guid%29?displayProperty=fullName> 오버로드로 지정하여 이 작업을 수행합니다. 이 작업이 성공한 경우 트랜잭션 기능이 제한됩니다. 비 MSDTC 트랜잭션 프로모터가 등록된 경우 다음 메서드는 MSDTC로의 승격이 필요하므로 <xref:System.Transactions.TransactionPromotionException>을 throw합니다.

- <xref:System.Transactions.Transaction.EnlistDurable%2A?displayProperty=fullName>

- <xref:System.Transactions.TransactionInterop.GetDtcTransaction%2A?displayProperty=fullName>

- <xref:System.Transactions.TransactionInterop.GetExportCookie%2A?displayProperty=fullName>

- <xref:System.Transactions.TransactionInterop.GetTransmitterPropagationToken%2A?displayProperty=fullName>

 비 MSDTC 트랜잭션 프로모터가 등록된 경우 향후 정의된 프로토콜을 사용하여 지속적인 인리스트먼트에 사용되어야 합니다. <xref:System.Transactions.Transaction.PromoterType%2A> 속성을 사용하여 트랜잭션 프로모터의 <xref:System.Guid>를 얻을 수 있습니다. 트랜잭션이 승격될 때 트랜잭션 프로모터는 승격된 토큰을 나타내는 <xref:System.Byte> 배열을 제공합니다. 응용 프로그램에서는 <xref:System.Transactions.Transaction.GetPromotedToken%2A> 메서드를 사용하여 비 MSDTC 승격된 트랜잭션에 대한 승격된 토큰을 가져올 수 있습니다.

 프로모션 작업을 성공적으로 완료하기 위해 새로운 <xref:System.Transactions.Transaction.EnlistPromotableSinglePhase%28System.Transactions.IPromotableSinglePhaseNotification%2CSystem.Guid%29?displayProperty=fullName> 오버로드의 사용자가 특정 호출 순서를 따라야 합니다. 이러한 규칙은 메서드 설명서에 나와 있습니다.

<a name="Profile461"></a> 
### <a name="profiling"></a>프로파일링
 관리되지 않는 프로파일링 API가 다음과 같이 개선되었습니다.

 [ICorProfilerInfo7](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md) 인터페이스에서 PDB 액세스에 대한 지원 개선. ASP.Net 5에서는 Roslyn에 의해 어셈블리가 메모리 내에서 컴파일되는 일이 더 많아지고 있습니다. 프로파일링 도구를 만드는 개발자에게 있어 이는 지금까지 디스크에 serialize되던 PDB가 더 이상 존재하지 않는다는 의미입니다. 프로파일러 도구는 종종 코드 검사 또는 줄 단위 성능 분석 등의 작업을 위해 PDB를 사용하여 코드를 다시 소스 줄에 매핑합니다. [ICorProfilerInfo7](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md) 인터 페이스는 [ICorProfilerInfo7::GetInMemorySymbolsLength](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-getinmemorysymbolslength-method.md)와 [ICorProfilerInfo7::ReadInMemorySymbols](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-readinmemorysymbols.md)의 두 가지 새로운 메서드를 포함합니다. 이 인터페이스에는 이제 메모리 내 PDB 데이터에 대한 액세스 권한과 함께 이러한 프로파일러 도구를 제공하는 새 메서드가 포함됩니다. 새 API를 사용하면 프로파일러가 메모리 내 PDB 콘텐츠를 바이트 배열로 가져온 다음 처리하거나 디스크로 직렬화할 수 있습니다.

 ICorProfiler 인터페이스를 사용하여 계측 향상. 동적 계측을 위해 `ICorProfiler` API의 ReJit 기능을 사용하는 프로파일러는 이제 일부 메타데이터를 수정할 수 있습니다. 이전에는 이러한 도구를 사용하여 언제든지 IL을 계측할 수 있었지만 메타데이터는 모듈 로드 시에만 수정할 수 있었습니다. IL은 메타데이터를 참조하므로 수행할 수 있는 계측 종류에 한계가 있었습니다. 모듈 로드 후의 메타데이터 하위 집합 편집을 지원하기 위해 [ICorProfilerInfo7::ApplyMetaData](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-applymetadata-method.md) 메서드를 추가하고 특히, 새 `AssemblyRef`, `TypeRef`, `TypeSpec`, `MemberRef`, `MemberSpec` 및 `UserString` 레코드를 추가하여 이러한 제한을 일부 상향했습니다. 이 변경을 통해 즉시 계측의 범위가 더 넓어졌습니다.

<a name="NGEN461"></a> 
### <a name="native-image-generator-ngen-pdbs"></a>NGEN(네이티브 이미지 생성기) PDB
 컴퓨터 간 이벤트 추적을 사용하면 고객이 시스템 A에서 프로그램을 프로파일링하고 소스 줄 매핑을 사용하여 시스템 B에서 프로파일링 데이터를 확인할 수 있습니다. 이전 버전의 .NET Framework에서는 사용자가 프로파일링된 시스템의 모든 모듈 및 네이티브 이미지를 IL PDB가 포함된 분석 시스템으로 복사하여 원본-네이티브 매핑을 만들었습니다. 이 프로세스는 휴대폰 응용 프로그램 등 비교적 파일이 작은 경우에는 잘 작동하지만 데스크톱 시스템에서는 파일이 매우 커질 수 있으며 복사하는 데 많은 시간이 필요합니다.

 Ngen PDB를 사용하면 NGen이 IL PDB에 대한 종속성 없이 IL-네이티브 매핑이 포함된 PDB를 만들 수 있습니다. 시스템 간 이벤트 추적 시나리오에서는 시스템 A에서 생성된 네이티브 이미지 PDB를 시스템 B로 복사하고 [Debug Interface Access API](https://msdn.microsoft.com/library/ee8x173s.aspx)를 사용하여 IL PDB의 소스-IL 매핑 및 네이티브 이미지 PDB의 IL-네이티브 매핑을 읽기만 하면 됩니다. 두 매핑을 함께 사용하면 소스-네이티브 매핑이 생성됩니다. 네이티브 이미지 PDB는 모든 모듈 및 네이티브 이미지보다 훨씬 작으므로 시스템 A에서 시스템 B로 복사하는 프로세스가 훨씬 빨라집니다.

<a name="v46"></a> 
## <a name="whats-new-in-net-2015"></a>.NET 2015의 새로운 기능
 .NET 2015에서는 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] 및 .NET Core가 도입되었습니다. 일부 새로운 기능은 둘 다에 적용되고 기타 기능은 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] 또는 [!INCLUDE[net_core](../../../includes/net-core-md.md)] 중 하나와 관련이 있습니다.

- **ASP.NET 5**

     .NET 2015에는 최신 클라우드 기반 앱을 빌드하기 위한 린(lean) .NET 플랫폼인 ASP.NET 5가 포함되어 있습니다. 이 플랫폼은 모듈식이므로 응용 프로그램에 필요한 기능만 포함할 수 있습니다. IIS에서 호스트되거나 사용자 지정 프로세스에서 자체 호스트될 수 있으며 동일한 서버에서 다양한 .NET Framework 버전으로 앱을 실행할 수 있습니다. 클라우드 배포용으로 설계된 새 환경 구성 시스템도 포함됩니다.

     MVC, Web API 및 웹 페이지가 MVC 6이라는 단일 프레임워크로 통합됩니다. Visual Studio 2015의 새로운 도구를 통해 ASP.NET 5 앱을 빌드합니다. 기존 응용 프로그램도 새로운 .NET Framework에서 작동하지만 MVC 6 또는 SignalR 3을 사용하는 앱을 빌드하려면 Visual Studio 2015의 프로젝트 시스템을 사용해야 합니다.

     자세한 내용은 [ASP.NET 5](http://go.microsoft.com/fwlink/?LinkId=518238)를 참조하십시오.

- **ASP.NET 업데이트**

    - **비동기 응답 플러시를 위한 작업 기반 API**

         이제 ASP.NET은 비동기 응답 플러시에 대한 간단한 작업 기반 API인 <xref:System.Web.HttpResponse.FlushAsync%2A?displayProperty=fullName>를 제공합니다. 이를 통해 해당 언어의 `async/await` 지원을 사용하여 응답을 비동기적으로 플러시할 수 있습니다.

    - `Model binding supports task-returning methods`

         [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에 ASP.NET이 Web Forms 페이지 및 사용자 정의 컨트롤에서 CRUD 기반 데이터 작업으로 확장 가능하고 코드 중심의 접근이 가능하도록 모델 바인딩 기능을 추가했습니다. 이제 모델 바인딩 시스템이 <xref:System.Threading.Tasks.Task>를 반환하는 모델 바인딩 메서드를 지원합니다. 이 기능으로 Web Forms 개발자가 Entity Framework를 포함하여 새 버전의 ORM을 사용하는 경우 간편한 데이터 바인딩 시스템과 함께 비동기의 확장성 이점을 얻을 수 있습니다.

         비동기 모델 바인딩은 `aspnet:EnableAsyncModelBinding` 구성 설정으로 제어합니다.

        ```
        <appSettings>
           <add key=" aspnet:EnableAsyncModelBinding" value="true|false" />
        </appSettings>
        ```

         [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]을 대상으로 하는 앱에서는 기본적으로 `true`입니다. 이전 버전의 .NET Framework를 대상으로 하고 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에서 실행되는 앱에서는 기본적으로 `false`입니다. 구성을 `true`로 설정하여 사용할 수 있습니다.

    - **HTTP/2 지원(Windows 10)**

         [HTTP/2](http://www.wikipedia.org/wiki/HTTP/2)는 더 나은 연결 사용률(클라이언트와 서버 간 왕복 횟수 감소)을 제공하여 사용자의 웹 페이지 로딩 대기 시간을 줄여주는 새 버전의 HTTP 프로토콜입니다.  이 프로토콜은 단일 환경의 일부로 요청되는 여러 아티팩트에 최적화되었으므로 웹 페이지(서비스 대비)가 HTTP/2에서 가장 많은 혜택을 얻을 수 있습니다. .NET Framework 4.6의 ASP.NET에는 HTTP/2 지원이 추가되었습니다. 여러 레이어에 네트워킹 기능이 있기 때문에 HTTP/2를 사용하려면 Windows, IIS 및 ASP.NET에 새로운 기능이 필요했습니다. ASP.NET과 함께 HTTP/2를 사용하려면 Windows 10에서 실행해야 합니다.

         또한 HTTP/2는 <xref:System.Net.Http.HttpClient?displayProperty=fullName> API를 사용하는 Windows 10 UWP(유니버설 Windows 플랫폼) 앱에서 지원되며 기본적으로 설정되어 있습니다.

         ASP.NET 응용 프로그램의 [PUSH_PROMISE](http://http2.github.io/http2-spec/#PUSH_PROMISE) 기능을 사용하는 방법을 제공하기 위해 두 가지 오버로드 <xref:System.Web.HttpResponse.PushPromise%28System.String%29> 및 <xref:System.Web.HttpResponse.PushPromise%28System.String%2CSystem.String%2CSystem.Collections.Specialized.NameValueCollection%29>을 사용하는 새 메서드가 <xref:System.Web.HttpResponse> 클래스에 추가되었습니다.

        > [!NOTE]
        >  ASP.NET 5는 HTTP/2를 지원하는 반면 PUSH PROMISE 기능에 대한 지원은 아직 추가되지 않았습니다.

         브라우저와 웹 서버(Windows의 IIS)가 모든 작업을 수행합니다. 사용자를 위해 직접 힘든 작업을 수행할 필요가 없습니다.

         대부분의 [주요 브라우저가 HTTP/2를 지원](http://www.wikipedia.org/wiki/HTTP/2)하므로 서버에서 지원할 경우 HTTP/2 지원은 사용자에게 도움이 될 수 있습니다.

    - **토큰 바인딩 프로토콜 지원**

         Microsoft 및 Google은 [토큰 바인딩 프로토콜](https://github.com/TokenBinding/Internet-Drafts)이라는 새로운 인증 방식을 위해 협력해 왔습니다. 전제 조건은 브라우저 캐시의 인증 토큰이 도난당해 범죄자가 암호나 기타 권한 있는 정보 없이도 보안 리소스(예: 은행 계좌)에 액세스하는 데 이용될 수 있다는 것입니다. 새 프로토콜은 이 문제를 완화시키기 위한 것입니다.

         토큰 바인딩 프로토콜은 Windows 10에서 브라우저 기능으로 구현됩니다. 인증 토큰이 정당한 것으로 검증되도록 ASP.NET 앱이 프로토콜에 참여합니다. 클라이언트와 서버 구현은 프로토콜에 의해 지정된 종단 간 보호를 설정합니다.

    - **임의 문자열 해시 알고리즘**

         .NET Framework 4.5에서는 [임의 문자열 해시 알고리즘](../configure-apps/file-schema/runtime/userandomizedstringhashalgorithm-element.md)이 도입되었습니다. 그러나 일부 ASP.NET 기능이 안정적인 해시 코드에 종속되어 있어 ASP.NET에서는 지원하지 않았습니다. 이제 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에서 임의 문자열 해시 알고리즘을 지원합니다. 이 기능을 사용하려면 `aspnet:UseRandomizedStringHashAlgorithm` 구성 설정을 사용합니다.

        ```
        <appSettings>
           <add key="aspnet:UseRandomizedStringHashAlgorithm" value="true|false" />
        </appSettings>
        ```

- **ADO.NET**

     ADO .NET은 이제 SQL Server 2016 CTP2(Community Technology Preview 2)에서 제공되는 상시 암호화 기능을 지원합니다. 항상 암호화 기능을 사용하면 SQL Server는 암호화된 데이터에 대해 작업을 수행할 수 있으며 무엇보다도, 암호화 키는 서버가 아니라 고객의 신뢰할 수 있는 환경 내에서 응용 프로그램과 함께 상주합니다. 항상 암호화 기능은 DBA가 일반 텍스트 데이터에 액세스할 수 없도록 고객 데이터를 보호합니다. 데이터 암호화 및 암호 해독은 드라이버 수준에서 투명하게 이루어지며 기존 응용 프로그램에 대한 변경을 최소화합니다. 자세한 내용은 [상시 암호화(데이터베이스 엔진)](/sql/relational-databases/security/encryption/always-encrypted-database-engine) 및 [상시 암호화(클라이언트 개발)](/sql/relational-databases/security/encryption/always-encrypted-client-development)를 참조하십시오.

- **관리 코드에 대한 64비트 JIT 컴파일러**

     .NET Framework 4.6에는 새 버전의64비트 JIT 컴파일러(원래 코드 이름은 RyuJIT)가 있습니다. 새로운 64비트 컴파일러는 이전 64비트 JIT 컴파일러보다 훨씬 향상된 성능을 제공합니다. 새로운 64비트 컴파일러는 .NET Framework 4.6에서 실행되는 64비트 프로세스에 사용됩니다. 앱이 64비트 또는 AnyCPU로 컴파일되고 64비트 운영 체제에서 실행되는 경우 해당 앱은 64비트 프로세스에서 실행됩니다. 새 컴파일러로 전환할 때 무슨 조치를 취했는지 투명하게 알 수 있으면 동작을 변경할 수 있습니다. 새 JIT 컴파일러를 사용할 때 발생하는 모든 문제에 대해 직접 듣고 싶습니다. 새로운 64비트 JIT 컴파일러와 관련된 문제가 발생하는 경우 [Microsoft Connect](http://connect.microsoft.com/)에 문의하십시오.

     또한 새로운 64비트 JIT 컴파일러에는 하드웨어 SIMD 가속 기능이 있으므로 <xref:System.Numerics> 네임스페이스의 SIMD 사용 형식과 함께 사용하면 성능이 현저히 향상될 수 있습니다.

- **어셈블리 로더 기능 향상**

     이제 어셈블리 로더가 해당 NGEN 이미지를 로드한 후 IL 어셈블리를 언로드하여 보다 효율적으로 메모리를 사용합니다. 이 변경으로 가상 메모리가 감소됩니다. 특히 큰 32비트 앱(예: Visual Studio)에 대해 효과적이며 실제 메모리도 절약됩니다.

- **기본 클래스 라이브러리 변경 내용**

     주요 시나리오를 사용할 수 있도록 많은 API가 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에 새로 추가되었습니다. 변경 및 추가된 내용은 다음과 같습니다.

    - **IReadOnlyCollection\<T> 구현**

         <xref:System.Collections.Generic.Queue%601> 및 <xref:System.Collections.Generic.Stack%601>을 포함한 추가 컬렉션이 <xref:System.Collections.Generic.IReadOnlyCollection%601>을 구현합니다.

    - **CultureInfo.CurrentCulture 및 CultureInfo.CurrentUICulture**

         <xref:System.Globalization.CultureInfo.CurrentCulture%2A?displayProperty=fullName> 및 <xref:System.Globalization.CultureInfo.CurrentUICulture%2A?displayProperty=fullName> 속성은 이제 읽기 전용 대신 읽기/쓰기로 설정됩니다. 이러한 속성에 새 <xref:System.Globalization.CultureInfo> 개체를 할당하면 `Thread.CurrentThread.CurrentCulture` 속성으로 정의된 현재 스레드 문화권과 `Thread.CurrentThread.CurrentUICulture` 속성으로 정의된 현재 UI 스레드 문화권도 변경됩니다.

    - **GC(가비지 수집) 향상**

         <xref:System.GC> 클래스는 이제 중요한 경로를 실행하는 동안 가비지 수집을 차단할 수 있는 <xref:System.GC.TryStartNoGCRegion%2A> 및 <xref:System.GC.EndNoGCRegion%2A> 메서드를 포함합니다.

         <xref:System.GC.Collect%28System.Int32%2CSystem.GCCollectionMode%2CSystem.Boolean%2CSystem.Boolean%29?displayProperty=fullName> 메서드의 새 오버로드를 통해 소형 개체 힙과 대형 개체 힙을 모두 정리하여 압축할지 또는 정리만 할지 제어할 수 있습니다.

    - **SIMD 사용 형식**

         <xref:System.Numerics> 네임스페이에는 이제 <xref:System.Numerics.Matrix3x2>, <xref:System.Numerics.Matrix4x4>, <xref:System.Numerics.Plane>, <xref:System.Numerics.Quaternion>, <xref:System.Numerics.Vector2>, <xref:System.Numerics.Vector3> 및 <xref:System.Numerics.Vector4> 등의 다양한 SIMD 사용 형식이 포함됩니다.

         또한 새로운 64비트 JIT 컴파일러에는 하드웨어 SIMD 가속 기능이 있으므로 SIMD 사용 형식과 새 64비트 JIT 컴파일러를 함께 사용하면 성능이 현저히 향상됩니다.

    - **암호화 업데이트**

         [Windows CNG 암호화 API](https://msdn.microsoft.com/library/windows/desktop/aa376214.aspx)를 지원하기 위해 <xref:System.Security.Cryptography?displayProperty=fullName> API가 업데이트됩니다. 이전 버전의 .NET Framework는 <xref:System.Security.Cryptography?displayProperty=fullName> 구현의 기반으로 [이전 버전의 Windows 암호화 API](https://msdn.microsoft.com/library/windows/desktop/aa380255.aspx)를 전적으로 사용했습니다. CNG API는 특정 범주의 앱에 중요한 [최신 암호화 알고리즘](https://msdn.microsoft.com/library/windows/desktop/bb204775.aspx#suite_b_support)을 지원하기 때문에 CNG API에 대한 지원 요청을 받았습니다.

         .NET Framework 4.6에는 Windows CNG 암호화 API를 지원하는 다음과 같은 새로운 향상 기능이 포함되어 있습니다.

        - X509 인증서에 대한 일련의 확장 메서드(`System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)` 및 `System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)`) - 가능한 경우 CAPI 기반 구현 대신 CNG 기반 구현을 반환합니다. (일부 스마트 카드 등에는 여전히 CAPI가 필요하며 API가 대체(fallback) 처리합니다.)

        - <xref:System.Security.Cryptography.RSACng?displayProperty=fullName> 클래스는 RSA 알고리즘의 CNG 구현을 제공합니다.

        - RSA API에 대한 향상 기능 - 일반 작업에 더 이상 캐스팅이 필요하지 않습니다. 예를 들어 <xref:System.Security.Cryptography.X509Certificates.X509Certificate2> 개체를 사용하여 데이터를 암호화하려면 이전 버전의 .NET Framework에서 다음과 같은 코드가 필요합니다.

             [!code-csharp[WhatsNew.Casting#1](../../../samples/snippets/csharp/VS_Snippets_CLR/whatsnew.casting/cs/program.cs#1)]
             [!code-vb[WhatsNew.Casting#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/whatsnew.casting/vb/module1.vb#1)]

             .NET Framework 4.6에서 새로운 암호화 API를 사용하는 코드는 캐스팅을 방지하기 위해 다음과 같이 작성될 수 있습니다.

             [!code-csharp[WhatsNew.Casting#2](../../../samples/snippets/csharp/VS_Snippets_CLR/whatsnew.casting/cs/program.cs#2)]
             [!code-vb[WhatsNew.Casting#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/whatsnew.casting/vb/module1.vb#2)]

    - **UNIX 시간으로/UNIX 시간에서 날짜 및 시간 변환 지원**

         다음의 새 메서드가 <xref:System.DateTimeOffset> 구조에 추가되어 UNIX 시간으로/UNIX 시간에서 날짜 및 시간 변환을 지원합니다.

        - <xref:System.DateTimeOffset.FromUnixTimeSeconds%2A?displayProperty=fullName>

        - <xref:System.DateTimeOffset.FromUnixTimeMilliseconds%2A?displayProperty=fullName>

        - <xref:System.DateTimeOffset.ToUnixTimeSeconds%2A?displayProperty=fullName>

        - <xref:System.DateTimeOffset.ToUnixTimeMilliseconds%2A?displayProperty=fullName>

    - **호환성 스위치**

         새 <xref:System.AppContext> 클래스는 라이브러리 작성자가 사용자에게 새로운 기능에 대한 균일한 옵트아웃(opt out) 메커니즘을 제공할 수 있게 해주는 새 호환성 기능을 추가합니다. 옵트아웃(opt out) 요청을 전달하기 위해 구성 요소 간에 느슨하게 결합된 계약을 설정합니다. 이 기능은 일반적으로 기존 기능이 변경될 때 중요합니다. 반대로, 새로운 기능에 대한 암시적 옵트인(opt in)은 이미 있습니다.

         <xref:System.AppContext>에서는 라이브러리가 호환성 스위치를 정의 및 노출하는 반면, 라이브러리에 종속된 코드가 해당 스위치를 설정하여 라이브러리 동작에 영향을 줄 수 있습니다. 기본적으로 라이브러리는 새로운 기능을 제공하며 스위치가 설정된 경우에만 변경합니다(즉, 이전 기능 제공).

         응용 프로그램(또는 라이브러리)은 종속 라이브러리가 정의하는 스위치 값(항상 <xref:System.Boolean> 값)을 선언할 수 있습니다. 스위치는 암시적으로 항상 `false`입니다. 스위치를 `true`로 설정하면 사용할 수 있습니다. 스위치를 명시적으로 `false`로 설정하면 새 동작이 제공됩니다.

        ```csharp
        AppContext.SetSwitch("Switch.AmazingLib.ThrowOnException", true);
        ```

         라이브러리는 소비자가 스위치 값을 선언했는지 확인한 다음 적절하게 동작해야 합니다.

        ```csharp
        if (!AppContext.TryGetSwitch("Switch.AmazingLib.ThrowOnException", out shouldThrow)) 
        {
           // This is the case where the switch value was not set by the application. 
           // The library can choose to get the value of shouldThrow by other means. 
           // If no overrides nor default values are specified, the value should be 'false'. 
           // A false value implies the latest behavior.
        }

           // The library can use the value of shouldThrow to throw exceptions or not.
           if (shouldThrow) 
           {
              // old code
           }
           else {
              // new code
           }
        }

        ```

         라이브러리에 의해 노출되는 공식 계약이므로 스위치에 대해 일관된 형식을 사용하는 것이 좋습니다. 다음은 두 가지 명확한 형식입니다.

        - *Switch*.*namespace*.*switchname*

        - *Switch*.*library*.*switchname*

    - **TAP(작업 기반 비동기 패턴) 변경 내용**

         [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]을 대상으로 하는 앱의 경우 <xref:System.Threading.Tasks.Task> 및 <xref:System.Threading.Tasks.Task%601> 개체는 문화권 및 호출 스레드의 UI 문화권을 상속합니다. 이전 버전의 .NET Framework를 대상으로 하거나 특정 버전의 .NET Framework를 대상으로 하지 않는 앱의 동작은 영향을 받지 않습니다. 자세한 내용은 <xref:System.Globalization.CultureInfo> 클래스 항목의 "문화권 및 작업 기반 비동기 작업" 섹션을 참조하십시오.

         <xref:System.Threading.AsyncLocal%601?displayProperty=fullName> 클래스를 사용하여 `async` 메서드와 같은 지정된 비동기 제어 흐름의 로컬 앰비언트 데이터를 나타낼 수 있습니다. 스레드 간에 데이터를 유지하는 데 사용할 수 있습니다. <xref:System.Threading.AsyncLocal%601.Value%2A?displayProperty=fullName> 속성이 명시적으로 변경되거나 스레드가 컨텍스트 전환을 발생시켜 앰비언트 데이터가 변경될 때마다 알림을 표시하는 콜백 메서드를 정의할 수도 있습니다.

         특정 상태에서 완료된 작업을 반환할 수 있도록 세 가지 편의 메서드 <xref:System.Threading.Tasks.Task.CompletedTask%2A?displayProperty=fullName>, <xref:System.Threading.Tasks.Task.FromCanceled%2A?displayProperty=fullName> 및 <xref:System.Threading.Tasks.Task.FromException%2A?displayProperty=fullName>이 TAP(작업 기반 비동기 패턴)에 추가되었습니다.

         <xref:System.IO.Pipes.NamedPipeClientStream> 클래스가 이제 새 <xref:System.IO.Pipes.NamedPipeClientStream.ConnectAsync%2A>와의 비동기 통신을 지원합니다. 메서드를 재정의합니다.

    - **EventSource에서 이벤트 로그에 쓰기 지원**

         이제 <xref:System.Diagnostics.Tracing.EventSource> 클래스를 사용하여 관리 또는 작동 메시지를 이벤트 로그와 컴퓨터에 만들어진 모든 기존 ETW 세션에 기록할 수 있습니다. 과거에는 이 기능을 위해 Microsoft.Diagnostics.Tracing.EventSource NuGet 패키지를 사용해야 했습니다. 이제 이 기능이 .NET Framework 4.6에 기본 제공됩니다.

         NuGet 패키지 및 .NET Framework 4.6이 다음 기능으로 업데이트되었습니다.

        - **동적 이벤트**

             이벤트 메서드를 만들지 않고 "즉시" 정의된 이벤트를 허용합니다.

        - **풍부한 페이로드**

             기본 형식뿐만 아니라 특별하게 특성이 정의된 클래스 및 배열이 페이로드로 전달될 수 있도록 허용합니다.

        - **작업 추적**

             시작과 중지 이벤트에서 현재 활성 중인 모든 작업을 나타내는 ID를 사용하여 이러한 이벤트 사이에서 발생하는 이벤트에 태그를 지정하도록 합니다.

         이러한 기능을 지원하기 위해 오버로드된 <xref:System.Diagnostics.Tracing.EventSource.Write%2A> 메서드가 <xref:System.Diagnostics.Tracing.EventSource> 클래스에 추가되었습니다.

- **WPF(Windows Presentation Foundation)**

    - **HDPI 기능 향상**

         이제 WPF의 HDPI 지원이 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에서 보다 향상되었습니다. 테두리가 있는 컨트롤에 클리핑 인스턴스를 줄이기 위해 레이아웃 반올림을 변경했습니다. 기본적으로 <xref:System.Runtime.Versioning.TargetFrameworkAttribute>가 .NET 4.6으러 설정된 경우에만 이 기능을 사용합니다.  이전 버전의 프레임워크를 대상으로 하지만 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에서 실행되는 응용 프로그램은 app.config 파일의 [\<runtime>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 섹션에 다음 줄을 추가하여 새 동작을 옵트인(opt in)할 수 있습니다.

        ```
        <AppContextSwitchOverrides
        value="Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false"
        />
        ```

         이제 서로 다른 DPI 설정(다중 DPI 설치)을 사용하여 여러 대의 모니터에 걸쳐 있는 WPF 창이 블랙아웃 영역 없이 완전하게 렌더링됩니다. 이 새로운 동작을 사용하지 않으려면 app.config 파일의 `<appSettings>` 섹션에 다음 줄을 추가하여 옵트아웃(opt out)할 수 있습니다.

        ```
        <add key="EnableMultiMonitorDisplayClipping" value="true"/>
        ```

         DPI 설정에 따라 오른쪽 커서를 자동으로 로딩하는 지원이 <xref:System.Windows.Input.Cursor?displayProperty=fullName>에 추가되었습니다.

    - **터치 기능 향상**

         고객이 터치 시 예기치 않은 동작이 발생한다고 [Connect](https://connect.microsoft.com/VisualStudio/feedback/details/903760/)에 신고한 문제가 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에서 해결되었습니다. 이제 Windows 스토어 응용 프로그램 및 WPF 응용 프로그램에 대한 두 번 탭하기 임계값이 Windows 8.1 이상 버전에서 같습니다.

    - **투명한 자식 창 지원**

         [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]의 WPF는 Windows 8.1 이상 버전에서 투명한 자식 창을 지원합니다. 이를 통해 최상위 창에서 사각형이 아닌 투명한 자식 창을 만들 수 있습니다. <xref:System.Windows.Interop.HwndSourceParameters.UsesPerPixelTransparency%2A?displayProperty=fullName> 속성을 `true`로 설정하여 이 기능을 사용할 수 있습니다.

- **WCF(Windows Communication Foundation)**

    - **SSL 지원**

         이제 WCF가 전송 보안 및 클라이언트 인증으로 NetTcp를 사용할 때 SSL 3.0 및 TLS 1.0뿐만 아니라 SSL 버전 TLS 1.1 및 TLS 1.2를 지원합니다. 이제 사용할 프로토콜을 선택하거나 이전의 안정성이 낮은 프로토콜을 사용하지 않도록 설정할 수 있습니다. <xref:System.ServiceModel.TcpTransportSecurity.SslProtocols%2A> 속성을 설정하거나 구성 파일에 다음을 추가하여 이 작업을 수행할 수 있습니다.

        ```
        <netTcpBinding>
           <binding>
              <security mode= "None|Transport|Message|TransportWithMessageCredential" >
                 <transport clientCredentialType="None|Windows|Certificate"
                            protectionLevel="None|Sign|EncryptAndSign"
                            sslProtocols="Ssl3|Tls1|Tls11|Tls12">
                    </transport>
              </security>
           </binding>
        </netTcpBinding>
        ```

    - **다른 HTTP 연결을 사용하여 메시지 전송**

         이제 WCF를 사용하여 사용자가 특정 메시지를 다른 기본 HTTP 연결을 사용하여 보낼 수 있습니다. 여기에는 두 가지 방법이 있습니다.

        - **연결 그룹 이름의 접두사 사용**

             사용자가 WCF에서 연결 그룹 이름의 접두사로 사용할 문자열을 지정할 수 있습니다. 서로 다른 접두사를 가진 두 메시지는 서로 다른 기본 HTTP 연결을 사용하여 보내집니다. 메시지의 <xref:System.ServiceModel.Channels.Message.Properties%2A?displayProperty=fullName> 속성에 키/값 쌍을 추가하여 접두사를 설정합니다. 키는 "HttpTransportConnectionGroupNamePrefix"이며 값은 원하는 접두사입니다.

        - **다른 채널 팩터리 사용**

             사용자는 서로 다른 채널 팩터리로 만들어진 채널을 사용하여 보낸 메시지가 서로 다른 기본 HTTP 연결을 사용하도록 하는 기능을 사용하도록 설정할 수도 있습니다. 이 기능을 사용하려면 사용자가 다음 `appSetting`을 `true`로 설정해야 합니다.

            ```
            <appSettings>
               <add key="wcf:httpTransportBinding:useUniqueConnectionPoolPerFactory" value="true" />
            </appSettings>
            ```

- **WWF(Windows Workflow Foundation)**

     이제 요청 시간이 초과되기 전에 처리 중인 "비 프로토콜" 책갈피가 있을 때 워크플로 서비스가 순서가 잘못된 작업 요청을 유지하는 시간을 초 단위로 지정할 수 있습니다. "비 프로토콜" 책갈피는 처리 중인 수신 작업에 관련되지 않은 책갈피입니다. 일부 작업은 구현되는 과정에서 비 프로토콜 책갈피를 만들기 때문에 비 프로토콜 책갈피가 있는지 정확히 알 수 없습니다. 여기에는 상태 및 선택이 포함됩니다. 따라서 워크플로 서비스를 상태 컴퓨터를 사용하여 구현하거나 선택 작업을 포함하여 구현한 경우 대부분 비 프로토콜 책갈피가 포함됩니다. app.config 파일의 `appSettings` 섹션에 다음과 같은 줄을 추가하여 간격을 지정합니다.

    ```
    <add key="microsoft:WorkflowServices:FilterResumeTimeoutInSeconds" value="60"/>
    ```

     기본값은 60초입니다. `value`가 0으로 설정되면 순서가 잘못된 요청은 다음과 같은 텍스트의 오류로 인해 즉시 거부됩니다.

    ```
    Operation 'Request3|{http://tempuri.org/}IService' on service instance with identifier '2b0667b6-09c8-4093-9d02-f6c67d534292' cannot be performed at this time. Please ensure that the operations are performed in the correct order and that the binding in use provides ordered delivery guarantees. 
    ```

     순서가 잘못된 작업 메시지를 수신하고 비 프로토콜 책갈피가 없다면 동일한 메시지를 수신한 것입니다.

     `FilterResumeTimeoutInSeconds` 요소의 값이 0이 아니고 비 프로토콜 책갈피가 있으며 시간 제한 간격이 만료된 경우 시간 초과 메시지와 함께 작업이 실패합니다.

- **트랜잭션**

     이제 <xref:System.Transactions.TransactionException>에서 파생된 예외를 throw한 트랜잭션의 분산 트랜잭션 식별자를 포함할 수 있습니다. 이렇게 하려면 app.config 파일의 `appSettings` 섹션에 다음 키를 추가합니다.

    ```
    <add key="Transactions:IncludeDistributedTransactionIdInExceptionMessage" value="true"/> 
    ```

     기본값은 `false`입니다.

- **네트워킹**

    - **소켓 재사용**

         Windows 10에는 새로운 확장성 높은 네트워킹 알고리즘이 있습니다. 이 알고리즘을 통해 아웃바운드 TCP 연결에 대한 로컬 포트를 재사용하여 컴퓨터 리소스를 효과적으로 사용할 수 있습니다. .NET Framework 4.6은 새 알고리즘을 지원하므로 .NET 앱이 새 동작을 활용할 수 있습니다. 이전 버전의 Windows에는 인위적인 동시 연결 제한(일반적으로 동적 포트 범위의 기본 크기는 16,384임)이 있었습니다. 이는 부하 상태에서 포트 소모를 발생시켜 서비스의 확장성을 제한할 수 있습니다.

         [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에는 두 개의 새 API가 추가되어 포트를 재사용할 수 있습니다. 이를 통해 동시 연결 시 64K 제한을 효과적으로 제거합니다.

        - <xref:System.Net.Sockets.SocketOptionName?displayProperty=fullName> 열거형 값.

        - <xref:System.Net.ServicePointManager.ReusePort%2A?displayProperty=fullName> 속성.

         `HKLM\SOFTWARE\Microsoft\.NETFramework\v4.0.30319` 등록 키의 `HWRPortReuseOnSocketBind` 값이 0x1으로 설정되어 있지 않으면 기본적으로 <xref:System.Net.ServicePointManager.ReusePort%2A?displayProperty=fullName> 속성은 `false`입니다. HTTP 연결에서 로컬 포트 재사용을 활성화하려면 <xref:System.Net.ServicePointManager.ReusePort%2A?displayProperty=fullName> 속성을 `true`로 설정하십시오. 이렇게 하면 <xref:System.Net.Http.HttpClient> 및 <xref:System.Net.HttpWebRequest>에서 나가는 모든 TCP 소켓 연결이 새 Windows 10 소켓 옵션인 [SO_REUSE_UNICASTPORT](https://msdn.microsoft.com/library/windows/desktop/ms740532.aspx)를 사용하여 로컬 포트를 재사용할 수 있습니다.

         소켓 전용 응용 프로그램을 제작하는 개발자는 바인딩하는 동안 아웃바운드 소켓이 로컬 포트를 재사용할 수 있도록 <xref:System.Net.Sockets.Socket.SetSocketOption%2A?displayProperty=fullName> 등의 메서드를 호출할 때 <xref:System.Net.Sockets.SocketOptionName?displayProperty=fullName> 옵션을 지정할 수 있습니다.

    - **국제 도메인 이름 및 PunyCode 지원**

         새 속성 <xref:System.Uri.IdnHost%2A>가 <xref:System.Uri> 클래스에 추가되어 국제 도메인 이름 및 PunyCode를 더욱 효과적으로 지원합니다.

- **Windows Forms 컨트롤 크기 조정.**

     이 기능은 [!INCLUDE[net_v46](../../../includes/net-v46-md.md)]에서 <xref:System.Windows.Forms.DomainUpDown>, <xref:System.Windows.Forms.NumericUpDown>, <xref:System.Windows.Forms.DataGridViewComboBoxColumn>, <xref:System.Windows.Forms.DataGridViewColumn> 및 <xref:System.Windows.Forms.ToolStripSplitButton> 형식과 <xref:System.Drawing.Design.UITypeEditor>를 그릴 때 사용되는 <xref:System.Drawing.Design.PaintValueEventArgs.Bounds%2A> 속성으로 지정된 사각형을 포함하도록 확장되었습니다.

     이 기능은 옵트인(opt-in) 기능입니다. 이 기능을 사용하려면 아래와 같이 응용 프로그램 구성 파일(app.config)에서 `EnableWindowsFormsHighDpiAutoResizing` 요소를 `true`로 설정해야 합니다.

    ```
    <appSettings>
       <add key="EnableWindowsFormsHighDpiAutoResizing" value="true" />
    </appSettings>
    ```

- **코드 페이지 인코딩 지원**

     [!INCLUDE[net_core](../../../includes/net-core-md.md)]에서는 주로 유니코드 인코딩을 지원하며, 기본적으로 코드 페이지 인코딩에 대한 제한된 지원을 제공합니다. <xref:System.Text.Encoding.RegisterProvider%2A?displayProperty=fullName> 메서드를 사용하여 코드 페이지 인코딩을 등록해 .NET Framework에서는 사용 가능하지만 [!INCLUDE[net_core](../../../includes/net-core-md.md)]에서는 지원되지 않는 코드 페이지 인코딩에 대한 지원을 추가할 수 있습니다. 자세한 내용은 <xref:System.Text.CodePagesEncodingProvider?displayProperty=fullName>를 참조 하세요.

- **.NET 네이티브**

     [!INCLUDE[net_core](../../../includes/net-core-md.md)]를 대상으로 하며 C# 또는 Visual Basic으로 작성된 Windows 10용 앱은 IL이 아니라 네이티브 코드로 앱을 컴파일하는 새 기술을 이용할 수 있습니다. 이렇게 생성된 앱은 시작 및 실행 시간이 훨씬 더 빠릅니다. 자세한 내용은 [.NET 네이티브로 앱 컴파일](../../../docs/framework/net-native/index.md)을 참조하십시오. JIT 컴파일 및 NGEN 둘 다와의 차이점 및 코드에 미치는 영향을 검사하는 .NET 네이티브의 개요는 [.NET 네이티브 및 컴파일](../../../docs/framework/net-native/net-native-and-compilation.md)을 참조하십시오.

     Visual Studio 2015로 컴파일하는 경우 앱은 기본적으로 네이티브 코드로 컴파일됩니다. 자세한 내용은 [.NET 네이티브 시작](../../../docs/framework/net-native/getting-started-with-net-native.md)을 참조하십시오.

     .NET 네이티브 앱 디버그를 지원하기 위해 다양한 인터페이스 및 열거형이 관리되지 않는 디버깅 API에 새로 추가되었습니다. 자세한 내용은 [디버깅(관리되지 않는 API 참조)](../../../docs/framework/unmanaged-api/debugging/index.md) 항목을 참조하십시오.

- **오픈 소스 .NET Framework 패키지**

     이제 [!INCLUDE[net_core](../../../includes/net-core-md.md)] 패키지(예: 변경할 수 없는 컬렉션, [SIMD API](http://go.microsoft.com/fwlink/?LinkID=518639)) 및 네트워킹 API(예: <xref:System.Net.Http> 네임스페이스에 있는 API)를 [GitHub](https://github.com/)에서 오픈 소스 패키지로 사용할 수 있습니다. 코드에 액세스하려면 [GitHub의 NetFx](http://go.microsoft.com/fwlink/?LinkID=518634)를 참조하십시오. 자세한 내용과 이러한 패키지에 기여하는 방법은 [.NET Core 및 오픈 소스](../../../docs/framework/get-started/net-core-and-open-source.md), [GitHub의 .NET 홈페이지](http://go.microsoft.com/fwlink/?LinkID=518635)를 참조하십시오.

 [맨 위로 이동](#introduction)

<a name="v452"></a> 
## <a name="whats-new-in-the-net-framework-452"></a>.NET Framework 4.5.2의 새로운 기능

- **ASP.NET 앱을 위한 새 API.** 새 <xref:System.Web.HttpResponse.AddOnSendingHeaders%2A?displayProperty=fullName> 및 <xref:System.Web.HttpResponseBase.AddOnSendingHeaders%2A?displayProperty=fullName> 메서드를 사용하면 응답이 클라이언트 앱으로 플러시될 때 응답 헤더 및 상태 코드를 검사하고 수정할 수 있습니다. <xref:System.Web.HttpApplication.PreSendRequestHeaders> 및 <xref:System.Web.HttpApplication.PreSendRequestContent> 이벤트보다 더욱 효율적이고 신뢰할 수 있는 이러한 메서드를 사용하는 것이 좋습니다.

     <xref:System.Web.Hosting.HostingEnvironment.QueueBackgroundWorkItem%2A?displayProperty=fullName> 메서드를 사용하면 작은 배경 작업 항목을 예약할 수 있습니다. ASP.NET는 이러한 항목을 추적하여 모든 백그라운드 작업 항목이 완료될 때까지는 IIS가 작업자 프로세스를 갑자기 종료하지 못하도록 합니다. ASP.NET 관리되는 앱 도메인 외부에서는 이 메서드를 호출할 수 없습니다.

     새 <xref:System.Web.HttpResponse.HeadersWritten?displayProperty=fullName> 및 <xref:System.Web.HttpResponseBase.HeadersWritten?displayProperty=fullName> 속성은 응답 헤더가 작성되었는지 여부를 나타내는 부울 값을 반환합니다. 이러한 속성을 사용하면 <xref:System.Web.HttpResponse.StatusCode%2A?displayProperty=fullName>(헤더가 작성되어 있으면 예외를 throw) 등의 API를 성공적으로 호출할 수 있습니다.

- **Windows Forms 컨트롤 크기 조정.** 이 기능은 확장되었습니다. 시스템 DPI 설정을 사용하여 다음과 같은 추가 컨트롤의 구성 요소 크기를 조정할 수 있습니다(예: 콤보 상자의 드롭다운 화살표).

     <xref:System.Windows.Forms.ComboBox>    <xref:System.Windows.Forms.ToolStripComboBox>    <xref:System.Windows.Forms.ToolStripMenuItem>    <xref:System.Windows.Forms.Cursor>    <xref:System.Windows.Forms.DataGridView>    <xref:System.Windows.Forms.DataGridViewComboBoxColumn>

     이 기능은 옵트인(opt-in) 기능입니다. 이 기능을 사용하려면 아래와 같이 응용 프로그램 구성 파일(app.config)에서 `EnableWindowsFormsHighDpiAutoResizing` 요소를 `true`로 설정해야 합니다.

    ```
    <appSettings>
       <add key="EnableWindowsFormsHighDpiAutoResizing" value="true" />
    </appSettings>
    ```

- **새 워크플로 기능.** <xref:System.Transactions.Transaction.EnlistPromotableSinglePhase%2A> 메서드를 사용하는 리소스 관리자(그에 따라 <xref:System.Transactions.IPromotableSinglePhaseNotification> 인터페이스 구현)는 새 <xref:System.Transactions.Transaction.PromoteAndEnlistDurable%2A?displayProperty=fullName> 메서드를 사용하여 다음을 요청할 수 있습니다.

    - 트랜잭션을 MSDTC(Microsoft Distributed Transaction Coordinator) 트랜잭션으로 승격합니다.

    - 단일 단계 커밋을 지원하는 지속적인 인리스트먼트인 <xref:System.Transactions.ISinglePhaseNotification>로 <xref:System.Transactions.IPromotableSinglePhaseNotification>을 대체합니다.

     이 기능은 동일한 앱 도메인 내에서 수행할 수 있으며 승격 수행을 위해 MSDTC와 상호 작용하기 위한 관리되지 않는 코드가 추가로 필요하지 않습니다. 새 메서드는 <xref:System.Transactions?displayProperty=fullName>에서, 승격 가능한 인리스트먼트로 구현되는 <xref:System.Transactions.IPromotableSinglePhaseNotification>`Promote` 메서드로의 처리되지 않은 호출이 있을 때만 호출할 수 있습니다.

- **프로파일링 기능 향상.** 다음과 같은 관리되지 않는 새로운 프로파일링 API를 통해 더욱 강력한 프로파일링 기능이 제공됩니다.

     [COR_PRF_ASSEMBLY_REFERENCE_INFO 구조](../../../docs/framework/unmanaged-api/profiling/cor-prf-assembly-reference-info-structure.md) 
     [COR_PRF_HIGH_MONITOR 열거형](../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) 
     [GetAssemblyReferences 메서드](../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) 
     [GetEventMask2 메서드](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-geteventmask2-method.md) 
     [SetEventMask2 메서드](../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) 
     [AddAssemblyReference 메서드](../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-addassemblyreference-method.md)

     이전 `ICorProfiler` 구현에서는 종속 어셈블리에 대한 지연 로딩이 지원되었습니다. 새로운 프로파일링 API의 경우 프로파일러에 의해 삽입된 종속 어셈블리는 앱이 완전히 초기화된 후에 로드되는 것이 아니라 즉시 로드할 수 있어야 합니다. 기존 `ICorProfiler` API 사용자에게는 이 변경 내용이 영향을 주지 않습니다.

- **디버깅 기능 향상.** 다음과 같은 관리되지 않는 새로운 디버깅 API를 통해 프로파일러와 더욱 완벽하게 통합할 수 있습니다. 덤프 디버깅 시 컴파일러 ReJIT 요청에 의해 생성된 로컬 변수 및 코드뿐 아니라 프로파일러가 삽입한 메타데이터를 액세스할 수 있습니다.

     [SetWriteableMetadataUpdateMode 메서드](../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-setwriteablemetadataupdatemode-method.md) 
     [EnumerateLocalVariablesEx 메서드](../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-enumeratelocalvariablesex-method.md) 
     [GetLocalVariableEx 메서드](../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getlocalvariableex-method.md) 
     [GetCodeEx 메서드](../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getcodeex-method.md) 
     [GetActiveReJitRequestILCode 메서드](../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-getactiverejitrequestilcode-method.md) 
     [GetInstrumentedILMap 메서드](../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md)

- **이벤트 추적 변경 내용.** .NET Framework 4.5.2에서는 대형 노출 영역에 대해 out-of-process로 실행되는 ETW(Windows용 이벤트 추적) 기반 작업 추적이 가능합니다. 이를 통해 APM(고급 전원 관리) 공급업체는 스레드 간의 각 요청 및 작업에 대한 비용을 정확하게 추적하는 간단한 도구를 제공할 수 있습니다.  이러한 이벤트는 ETW 컨트롤러에 의해 활성화된 경우에만 발생되므로 이전에 작성된 ETW 코드나 비활성화된 ETW로 실행된 코드에는 변경 내용이 적용되지 않습니다.

- **트랜잭션을 승격하고 지속적인 인리스트먼트로 변환**

     <xref:System.Transactions.Transaction.PromoteAndEnlistDurable%2A?displayProperty=fullName>은 다음과 같이 .NET Framework 4.5.2 및 4.6에 추가된 새 API입니다.

    ```csharp
    [System.Security.Permissions.PermissionSetAttribute(System.Security.Permissions.SecurityAction.LinkDemand, Name = "FullTrust")]
    public Enlistment PromoteAndEnlistDurable(Guid resourceManagerIdentifier,
                                              IPromotableSinglePhaseNotification promotableNotification,
                                              ISinglePhaseNotification enlistmentNotification,
                                              EnlistmentOptions enlistmentOptions)
    ```

     해당 메서드는 이전에 <xref:System.Transactions.ITransactionPromoter.Promote%2A?displayProperty=fullName> 메서드에 대한 응답으로 <xref:System.Transactions.Transaction.EnlistPromotableSinglePhase%2A?displayProperty=fullName>가 만든 인리스트먼트가 사용할 수 있습니다. 트랜잭션을 MSDTC 트랜잭션으로 승격하고 승격할 수 있는 인리스트먼트를 지속적인 인리스트먼트로 "변환"하도록 `System.Transactions`에게 요청합니다. 이 메서드가 성공적으로 완료된 후에는 `System.Transactions`이 더 이상 <xref:System.Transactions.IPromotableSinglePhaseNotification> 인터페이스를 참조하지 않으며 이후의 모든 알림은 제공된 <xref:System.Transactions.ISinglePhaseNotification> 인터페이스에 도착합니다. 해당 인리스트먼트는 지속적인 인리스트먼트로 작동해야 하며 트랜잭션 로깅 및 복구를 지원합니다. 자세한 내용은 <xref:System.Transactions.Transaction.EnlistDurable%2A?displayProperty=fullName>을 참조하십시오. 또한 인리스트먼트는 <xref:System.Transactions.ISinglePhaseNotification>.</xref:System.Transactions.ISinglePhaseNotification>을 지원해야 합니다.  이 메서드는 <xref:System.Transactions.ITransactionPromoter.Promote%2A?displayProperty=fullName> 호출을 처리하는 동안에 *오직* 호출을 받는 것만 가능합니다. 그렇지 않은 경우 <xref:System.Transactions.TransactionException> 예외가 throw됩니다.

 [맨 위로 이동](#introduction)

<a name="v451"></a> 
## <a name="whats-new-in-the-net-framework-451"></a>.NET Framework 4.5.1의 새로운 기능
 **2014년 4월 업데이트**:

- [Visual Studio 2013 업데이트 2](http://go.microsoft.com/fwlink/p/?LinkId=393658)에는 이식 가능한 클래스 라이브러리 템플릿에 대한 업데이트가 포함되어 다음과 같은 시나리오가 지원됩니다.

    - Windows 8.1, Windows Phone 8.1 및 Windows Phone Silverlight 8.1을 대상으로 하는 이식 가능한 라이브러리에서 Windows 런타임 API를 사용할 수 있습니다.

    - Windows 8.1 또는 Windows Phone 8.1을 대상으로 하는 경우 XAML(Windows.UI.XAML 형식)을 이식 가능한 라이브러리에 포함할 수 있습니다. XAML 템플릿(빈 페이지, 리소스 사전, 템플릿 컨트롤 및 사용자 정의 컨트롤)이 지원됩니다.

    - Windows 8.1 및 Windows Phone 8.1 대상의 스토어 앱에서 사용할 이식 가능한 Windows 런타임 구성 요소(.winmd 파일)를 만들 수 있습니다.

    - 이식 가능한 클래스 라이브러리처럼 대상을 다시 Windows 스토어 또는 Windows Phone 스토어 클래스 라이브러리를 변경할 수 있습니다.

     이러한 변경 내용에 대한 자세한 내용은 [이식 가능한 클래스 라이브러리](../../../docs/standard/cross-platform/cross-platform-development-with-the-portable-class-library.md)을 참조하십시오.

- 이제 Windows 앱 빌드 및 배포를 위한 미리 컴파일 기술인 [!INCLUDE[net_native](../../../includes/net-native-md.md)]에 대한 설명서가 .NET Framework 콘텐츠 집합에 포함되었습니다. [!INCLUDE[net_native](../../../includes/net-native-md.md)]는 앱을 중간 언어가 아닌 네이티브 코드로 직접 컴파일하여 더 나은 성능을 제공합니다. 자세한 내용은 [.NET 네이티브로 앱 컴파일](../../../docs/framework/net-native/index.md)을 참조하십시오.

- [.NET Framework 참조 소스](http://referencesource.microsoft.com/)에서는 새로운 검색 환경과 향상된 기능을 제공합니다. 온라인에서 .NET Framework 소스 코드를 검색하여, [참조를 다운로드](http://referencesource.microsoft.com/download.html)해 오프라인에서 살펴보고, 디버그 시 소스(패치 및 업데이트 포함)를 단계별로 실행할 수 있습니다. 자세한 내용은 블로그 항목 [.NET 참조 소스의 새로운 디자인](https://blogs.msdn.microsoft.com/dotnet/2014/02/24/a-new-look-for-net-reference-source/)을 참조하십시오.

 .NET Framework 4.5.1의 주요 새로운 기능 및 향상된 기능은 다음과 같습니다.

- 어셈블리에 대한 자동 바인딩 리디렉션. [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]부터는 [!INCLUDE[net_v451](../../../includes/net-v451-md.md)]을 대상으로 하는 응용 프로그램을 컴파일할 때 응용 프로그램 또는 해당 구성 요소가 동일한 어셈블리의 여러 버전을 참조할 경우 응용 프로그램 구성 파일에 바인딩 리디렉션을 추가할 수 있습니다. 또한 이전 버전의 .NET Framework를 대상으로 하는 프로젝트에 대해 이 기능을 사용하도록 설정할 수 있습니다. 자세한 내용은 [방법: 자동 바인딩 리디렉션 사용 설정 및 해제](../../../docs/framework/configure-apps/how-to-enable-and-disable-automatic-binding-redirection.md)를 참조하십시오.

- 진단 정보를 수집하여 개발자가 서버 및 클라우드 응용 프로그램의 성능을 향상시키는 기능. 자세한 내용은 <xref:System.Diagnostics.Tracing.EventSource>클래스의 <xref:System.Diagnostics.Tracing.EventSource.WriteEventWithRelatedActivityId%2A> 및 <xref:System.Diagnostics.Tracing.EventSource.WriteEventWithRelatedActivityIdCore%2A> 메서드를 참조하십시오.

- 가비지 수집 동안 LOH(대형 개체 힙)를 명시적으로 압축하는 기능. 자세한 내용은 <xref:System.Runtime.GCSettings.LargeObjectHeapCompactionMode%2A?displayProperty=fullName>속성을 참조하십시오.

- .NET Framework 업데이트를 통해 ASP.NET 응용 프로그램 일시 중단, 멀티 코어 JIT 개선 및 빠른 응용 프로그램 시작 등의 추가적인 성능 개선. 자세한 내용은 [.NET Framework 4.5.1 알림](https://blogs.msdn.microsoft.com/dotnet/2013/06/26/announcing-the-net-framework-4-5-1-preview/) 및 [ASP.NET 응용 프로그램 일시 중단](https://blogs.msdn.microsoft.com/dotnet/2013/10/09/asp-net-app-suspend-responsive-shared-net-web-hosting/) 블로그 게시물을 참조하십시오.

 Windows Forms의 향상된 기능은 다음과 같습니다.

- Windows Forms 컨트롤 크기 조정. 앱의 응용 프로그램 구성 파일(app.config)의 항목을 선택하여 시스템 DPI 설정으로 컨트롤 구성 요소(예: 속성 표에 표시되는 아이콘)의 크기를 조정할 수 있습니다. 이 기능은 현재 다음과 같은 Windows Forms 컨트롤에서 지원됩니다.

     <xref:System.Windows.Forms.PropertyGrid>    <xref:System.Windows.Forms.TreeView>    <xref:System.Windows.Forms.DataGridView>의 일부 구성 요소(그 밖에 지원되는 컨트롤에 대해서는 [4.5.2의 새로운 기능](#v452) 참조)

     이 기능을 사용하려면 다음과 같이 새로운 \<appSettings> 요소를 구성 파일(app.config)에 추가하여 `EnableWindowsFormsHighDpiAutoResizing` 요소를 `true`로 설정합니다.

    ```
    <appSettings>
       <add key="EnableWindowsFormsHighDpiAutoResizing" value="true" />
    </appSettings>
    ```

 [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]의 .NET Framework 응용 프로그램 디버깅 시 개선된 기능은 다음과 같습니다.

- Visual Studio 디버거에서 값 반환. [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]에서 관리되는 응용 프로그램을 디버깅하면 자동 창에 메서드에 대한 반환 형식 및 값이 표시됩니다. 이 정보는 데스크톱, Windows 스토어 및 Windows Phone 응용 프로그램에서 사용할 수 있습니다. 자세한 내용은 MSDN 라이브러리의 [메서드 호출의 반환 값 검사](http://msdn.microsoft.com/library/e3245b37-8e2e-4200-ba84-133726e95f1f\(v=vs.120\).aspx)를 참조하십시오.

- 64비트 응용 프로그램의 편집하며 계속하기. [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]은 데스크톱, Windows 스토어 및 Windows Phone용 64비트 관리되는 응용 프로그램의 편집하며 계속하기 기능을 지원합니다. 기존 제한은 32비트 응용 프로그램과 64비트 응용 프로그램에서 그대로 적용됩니다. [지원되는 코드 변경 내용(C#)](/visualstudio/debugger/supported-code-changes-csharp) 문서의 마지막 섹션을 참조하십시오.

- 비동기 인식 디버깅. [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]에서 비동기 응용 프로그램을 더 쉽게 디버깅하기 위해 호출 스택은 컴파일러에서 제공된 인프라 코드를 숨겨 비동기 프로그래밍을 지원하고, 논리 프로그램 실행을 보다 명확하게 반영할 수 있도록 논리 부모 프레임의 체인을 숨깁니다. 병렬 작업 창은 작업 창으로 대체되고 특정 중단점과 관련된 작업을 표시하며 응용 프로그램에서 현재 활성 상태이거나 예약된 다른 작업도 모두 표시합니다. 이 기능에 대한 자세한 내용을 [.NET Framework 4.5.1 알림](https://blogs.msdn.microsoft.com/dotnet/2013/06/26/announcing-the-net-framework-4-5-1-preview/)의 "비동기 인식 디버깅" 섹션에서 확인할 수 있습니다.

- Windows 런타임 구성 요소에 대한 예외 지원 향상. [!INCLUDE[win81](../../../includes/win81-md.md)]에서는 다른 언어 간에도 예외의 원인인 오류에 대한 정보를 Windows 스토어 응용 프로그램에서 발생시킨 예외에 보존합니다. 이 기능에 대한 자세한 내용을 [.NET Framework 4.5.1 알림](https://blogs.msdn.microsoft.com/dotnet/2013/06/26/announcing-the-net-framework-4-5-1-preview/)의 "Windows 스토어 앱 개발" 섹션에서 확인할 수 있습니다. 

 [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]부터 [관리되는 프로필 기반 최적화 도구(Mpgo.exe)](../../../docs/framework/tools/mpgo-exe-managed-profile-guided-optimization-tool.md)를 사용하여 [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 앱과 데스크톱 앱을 최적화할 수 있습니다.

 ASP.NET 4.5.1의 새로운 기능은 ASP.NET 사이트의 [ASP.NET 4.5.1 및 Visual Studio 2013](http://go.microsoft.com/fwlink/?LinkID=309094)을 참조하십시오.

 [맨 위로 이동](#introduction)

<a name="core"></a> 
## <a name="whats-new-in-the-net-framework-45"></a>.NET Framework 4.5의 새로운 기능

### <a name="core-new-features-and-improvements"></a>주요 새로운 기능 및 향상된 기능

- 배포 시 .NET Framework 4 응용 프로그램을 감지하고 닫아 시스템 다시 시작 횟수를 줄이는 기능. [.NET Framework 4.5를 설치하는 동안 시스템 다시 시작 줄이기](../../../docs/framework/deployment/reducing-system-restarts.md)를 참조하십시오.

- 64비트 플랫폼에서 2GB보다 큰 배열 지원. 응용 프로그램 구성 파일에서 이 기능을 사용하도록 설정할 수 있습니다. 개체 크기와 배열 크기에 대한 기타 제한을 나열하는 [\<gcAllowVeryLargeObjects> 요소](../../../docs/framework/configure-apps/file-schema/runtime/gcallowverylargeobjects-element.md)를 참조하십시오.

- 서버에 대한 백그라운드 가비지 수집을 통해 성능 향상. 사용자가 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에서 서버 가비지 수집을 사용하면 백그라운드 가비지 수집을 사용하도록 자동으로 설정됩니다. [가비지 컬렉션 기본 사항](../../../docs/standard/garbage-collection/fundamentals.md) 항목의 백그라운드 서버 가비지 컬렉션 섹션을 참조하십시오.

- 응용 프로그램 성능 개선을 위해 다중 코어 프로세서에서 선택적으로 사용 가능한 백그라운드 JIT(Just-In-Time) 컴파일. <xref:System.Runtime.ProfileOptimization>을 참조하십시오.

- 정규식 엔진이 시간 초과되기 전에 정규식 해결을 시도하는 시간을 제한하는 기능. <xref:System.Text.RegularExpressions.Regex.MatchTimeout%2A?displayProperty=fullName> 속성을 참조하십시오.

- 응용 프로그램 도메인에 대한 기본 문화권을 정의하는 기능. <xref:System.Globalization.CultureInfo> 클래스를 참조하십시오.

- 콘솔에서 유니코드(UTF-16) 인코딩 지원. <xref:System.Console> 클래스를 참조하십시오.

- 문화권 문자열 순서 지정 및 비교 데이터의 버전 관리 지원. <xref:System.Globalization.SortVersion> 클래스를 참조하십시오.

- 리소스 검색 시 성능 향상. [리소스 패키징 및 배포](../../../docs/framework/resources/packaging-and-deploying-resources-in-desktop-apps.md)를 참조하십시오.

- 압축 파일의 크기를 줄이기 위해 zip 압축 기능 개선. <xref:System.IO.Compression?displayProperty=fullName> 네임스페이스를 참조하십시오.

- <xref:System.Reflection.Context.CustomReflectionContext> 클래스를 통해 기본 리플렉션 동작을 재정의하도록 리플렉션 컨텍스트를 사용자 지정하는 기능.

- [!INCLUDE[win8](../../../includes/win8-md.md)]에서 <xref:System.Globalization.IdnMapping?displayProperty=fullName> 클래스 사용 시 IDNA(Internationalizing Domain Names in Applications) 표준의 2008 버전을 지원합니다.

- .NET Framework가 [!INCLUDE[win8](../../../includes/win8-md.md)]에서 사용되면 유니코드 6.0을 구현하는 문자열 비교가 운영 체제에 위임됨. 다른 플랫폼에서 실행되는 경우 유니코드 5.x를 구현하는 자체 문자열 비교 데이터가 .NET Framework에 포함됩니다. <xref:System.String>클래스 및 <xref:System.Globalization.SortVersion>클래스의 설명 섹션을 참조하십시오.

- 응용 프로그램 도메인 단위로 문자열에 대한 해시 코드를 계산하는 기능. [\<<UseRandomizedStringHashAlgorithm> 요소](../../../docs/framework/configure-apps/file-schema/runtime/userandomizedstringhashalgorithm-element.md)를 참조하십시오.

- 형식 반사는 <xref:System.Type>과 <xref:System.Reflection.TypeInfo> 클래스 간에 분할을 지원합니다. [Windows 스토어 앱에 대한 .NET Framework의 리플렉션](../../../docs/framework/reflection-and-codedom/reflection-for-windows-store-apps.md)을 참조하십시오.

### <a name="managed-extensibility-framework-mef"></a>MEF(Managed Extensibility Framework)
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]의 MEF(Managed Extensibility Framework)는 다음과 같은 새로운 기능을 제공합니다.

- 제네릭 형식 지원

- 특성이 아닌 명명 규칙을 기반으로 파트를 만들 수 있는 규칙 기반 프로그래밍 모델

- 다중 범위

- [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 응용 프로그램을 만들 때 사용할 수 있는 MEF의 하위 집합. 이 하위 집합은 NuGet 갤러리에서 [다운로드 가능 패키지](http://go.microsoft.com/fwlink/?LinkId=256238)로 사용할 수 있습니다. 패키지를 설치하려면 Visual Studio에서 프로젝트를 열고 **프로젝트** 메뉴에서 **NuGet 패키지 관리**를 선택한 후 `Microsoft.Composition` 패키지를 온라인으로 검색합니다.

 자세한 내용은 [MEF(관리되는 확장성 프레임워크 개요)](../../../docs/framework/mef/index.md)를 참조하십시오.

### <a name="asynchronous-file-operations"></a>비동기 파일 작업
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에서는 C# 및 Visual Basic 언어에 새로운 비동기 기능이 추가되었습니다. 이러한 기능은 비동기 작업을 수행하는 작업 기반 모델을 추가합니다. 이 새로운 모델을 사용하려면 I/O 클래스에서 비동기 메서드를 사용합니다. [비동기 파일 I/O](../../../docs/standard/io/asynchronous-file-i-o.md)를 참조하십시오.

<a name="tools"></a> 
### <a name="tools"></a>도구
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에서 리소스 파일 생성기(Resgen.exe)를 사용하면 .NET Framework 어셈블리에 포함된 .resources 파일에서 [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 응용 프로그램에 사용할 .resw 파일을 만들 수 있습니다. 자세한 내용은 [Resgen.exe(리소스 파일 생성기)](../../../docs/framework/tools/resgen-exe-resource-file-generator.md)를 참조하십시오.

 관리되는 프로필 기반 최적화(Mpgo.exe)를 사용하면 네이티브 이미지 어셈블리를 최적화하여 응용 프로그램 시작 시간, 메모리 사용률(작업 집합 크기) 및 처리량을 개선할 수 있습니다. 명령줄 도구는 네이티브 이미지 응용 프로그램 어셈블리에 대한 프로필 데이터를 생성합니다. [Mpgo.exe(관리되는 프로필 기반 최적화 도구)](../../../docs/framework/tools/mpgo-exe-managed-profile-guided-optimization-tool.md)를 참조하십시오. [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)]부터는 Mpgo.exe를 사용하여 [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 응용 프로그램과 데스크톱 응용 프로그램을 최적화할 수 있습니다.

<a name="parallel"></a> 
### <a name="parallel-computing"></a>병렬 컴퓨팅
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]는 병렬 컴퓨팅을 위한 몇 가지 새로운 기능과 향상된 기능을 제공합니다. 여기에는 성능 향상, 제어 강화, 비동기 프로그래밍에 대한 지원 개선, 새 데이터 흐름 라이브러리 및 병렬 디버깅 및 성능 분석에 대한 지원 개선이 포함됩니다. .NET 블로그에서 병렬 프로그래밍에 대한 항목인 [.NET 4.5의 새로운 병렬 처리 기능](http://go.microsoft.com/fwlink/?LinkId=235061)을 참조하십시오.

<a name="web"></a> 
### <a name="web"></a>웹
 ASP.NET 4.5 및 4.5.1은 Web Forms, WebSocket 지원, 비동기 처리기, 성능 향상 및 기타 많은 기능을 바인딩하는 모델을 추가합니다. 자세한 내용은 다음 리소스를 참조하세요.

- MSDN 라이브러리의 [ASP.NET 4.5 및 Visual Studio 2012](http://msdn.microsoft.com/library/ac9bb7f6-f094-4af7-bad0-acf49a5dbc55)

- ASP.NET 사이트의 [ASP.NET 4.5.1 및 Visual Studio 2013](http://go.microsoft.com/fwlink/?LinkID=309094)

<a name="networking"></a> 
### <a name="networking"></a>네트워킹
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에서는 HTTP 응용 프로그램의 새로운 프로그래밍 인터페이스를 제공합니다. 자세한 내용은 새로운 <xref:System.Net.Http?displayProperty=fullName> 및 <xref:System.Net.Http.Headers?displayProperty=fullName> 네임스페이스를 참조하십시오.

 기존의 <xref:System.Net.HttpListener> 및 관련 클래스를 사용하여 WebSocket 연결을 허용하고 이와 상호 작용하는 새로운 프로그래밍 인터페이스 지원도 포함되어 있습니다. 자세한 내용은 새로운 <xref:System.Net.WebSockets> 네임스페이스 및 <xref:System.Net.HttpListener> 클래스를 참조하십시오.

 또한 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에는 다음 네트워킹 개선 사항이 포함되어 있습니다.

- RFC 규격 URI 지원. 자세한 내용은 <xref:System.Uri> 및 관련 클래스를 참조하십시오.

- IDN(Internationalized Domain Name) 구문 분석 지원. 자세한 내용은 <xref:System.Uri> 및 관련 클래스를 참조하십시오.

- EAI(Email Address Internationalization) 지원. 자세한 내용은 <xref:System.Net.Mail> 네임스페이스를 참조하십시오.

- IPv6 지원 개선. 자세한 내용은 <xref:System.Net.NetworkInformation> 네임스페이스를 참조하십시오.

- 이중 모드 소켓 지원. 자세한 내용은 <xref:System.Net.Sockets.Socket> 및 <xref:System.Net.Sockets.TcpListener>클래스를 참조하십시오.

<a name="client"></a> 
### <a name="windows-presentation-foundation-wpf"></a>WPF(Windows Presentation Foundation)
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]의 WPF(Windows Presentation Foundation)에서 변경되고 개선된 영역은 다음과 같습니다.

- 빠른 실행 도구 모음, 응용 프로그램 메뉴 및 탭을 호스팅하는 리본 사용자 인터페이스 구현에 사용할 수 있는 새로운 <xref:System.Windows.Controls.Ribbon.Ribbon> 컨트롤

- 동기 및 비동기 데이터 유효성 검사를 지원하는 새로운 <xref:System.ComponentModel.INotifyDataErrorInfo> 인터페이스

- <xref:System.Windows.Controls.VirtualizingPanel> 및 <xref:System.Windows.Threading.Dispatcher> 클래스에 대한 새 기능

- 그룹화된 큰 데이터 집합을 표시하고 UI가 아닌 스레드에서 컬렉션에 액세스할 때의 성능 개선

- 정적 속성에 대한 데이터 바인딩, <xref:System.Reflection.ICustomTypeProvider> 인터페이스를 구현하는 사용자 지정 형식에 대한 데이터 바인딩 및 바인딩 식에서 데이터 바인딩 정보 검색

- 값이 변경될 때(라이브 셰이핑) 데이터의 위치 변경

- 항목 컨테이너에 대한 데이터 컨텍스트 연결을 해제할지 여부를 확인하는 기능

- 속성 변경과 데이터 소스 업데이트 간에 경과되어야 하는 시간을 설정하는 기능

- 취약한 이벤트 패턴을 구현하기 위한 지원 개선. 또한 이벤트가 태그 확장을 수락할 수 있습니다.

<a name="windows_communication_foundation"></a> 
### <a name="windows-communication-foundation-wcf"></a>WCF(Windows Communication Foundation)
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에서 WCF(Windows Communication Foundation) 응용 프로그램을 더 쉽게 작성하고 유지 관리할 수 있도록 다음 기능이 추가되었습니다.

- 생성된 구성 파일의 단순화

- 계약 중심 개발 지원

- ASP.NET 호환성 모드를 더 쉽게 구성하는 기능

- 기본 전송 속성 값을 변경하여 값을 설정해야 할 가능성을 줄임

- <xref:System.Xml.XmlDictionaryReaderQuotas> 클래스를 업데이트하여 XML 사전 판독기에 대해 수동으로 할당량을 구성해야 할 가능성을 줄임

- Visual Studio에서 빌드 프로세스의 일부로 WCF 구성 파일의 유효성 검사를 실시하여 응용 프로그램 실행 전에 구성 오류를 검색할 수 있도록 함

- 새로운 비동기 스트리밍 지원

- 새 HTTPS 프로토콜 매핑을 사용하면 간단하게 IIS(인터넷 정보 서비스)로 HTTPS에서 끝점을 표시할 수 있음

- 서비스 URL에 `?singleWSDL`을 추가하여 단일 WSDL 문서에서 메타데이터를 생성하는 기능

- Websocket이 포트 80 및 443에서 완벽한 양방향 통신을 지원하며 성능 특성은 TCP 전송과 유사함

- 코드에서 서비스 구성 지원

- XML 편집기 도구 설명

- <xref:System.ServiceModel.ChannelFactory> 캐싱 지원

- 이진 인코더 압축 지원

- 개발자가 "실행 후 제거" 메시징을 사용하는 서비스를 작성할 수 있는 UDP 전송 지원. 클라이언트는 서비스에 메시지를 보내고 서비스에서 응답을 기대하지 않습니다.

- HTTP 전송 및 전송 보안 사용 시 단일 WCF 끝점에 대한 여러 인증 모드를 지원하는 기능

- IDN(Internationalized Domain Name)을 사용하는 WCF 서비스 지원

 자세한 내용은 [Windows Communication Foundation의 새로운 기능](http://go.microsoft.com/fwlink/?LinkId=228173)을 참조하십시오.

<a name="windows_workflow_foundation"></a> 
### <a name="windows-workflow-foundation-wf"></a>Windows WF(Workflow Foundation)
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]의 Windows WF(Workflow Foundation)에 몇 가지 새로운 기능이 추가되었습니다.

- 상태 시스템 워크플로가 .NET Framework 4.0.1([.NET Framework 4 플랫폼 업데이트 1](http://go.microsoft.com/fwlink/?LinkID=215092))의 일부로 처음 도입됨. 이 업데이트에는 개발자가 상태 시스템 워크플로를 만들 수 있도록 하는 몇 가지 새로운 클래스와 활동이 포함되었습니다. 이러한 클래스와 활동은 다음을 포함하도록 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)]에 대해 업데이트되었습니다.

    - 상태에 중단점을 설정하는 기능

    - Workflow Designer에서 전환을 복사하여 붙여 넣는 기능

    - 공유 트리거 전환 작성을 위한 디자이너 지원

    - <xref:System.Activities.Statements.StateMachine>, <xref:System.Activities.Statements.State> 및 <xref:System.Activities.Statements.Transition>을 비롯하여 상태 시스템 워크플로를 만들기 위한 활동

- 다음과 같은 향상된 Workflow Designer 기능

    - Visual Studio의 **빠른 찾기** 및 **파일에서 찾기** 등의 향상된 워크플로 검색 기능

    - 컨테이너 활동에 두 번째 자식 활동이 추가될 때 Sequence 활동을 자동으로 생성하고 두 활동 모두를 Sequence 활동에 포함하는 기능

    - 스크롤 막대를 사용하지 않고 워크플로의 보이는 부분을 변경할 수 있는 이동 기능 지원

    - 트리 스타일 개요 뷰에서 워크플로의 구성 요소를 보여 주는 새로운 **문서 개요** 뷰. 이 **문서 개요** 뷰에서 구성 요소를 선택할 수 있음

    - 활동에 주석을 추가하는 기능

    - Workflow Designer를 사용하여 활동 대리자를 정의하고 사용하는 기능

    - 상태 시스템과 순서도 워크플로에서 활동 및 전환의 자동 연결 및 자동 삽입

- XAML 파일의 단일 요소에 워크플로의 뷰 상태 정보가 저장되므로 뷰 상태 정보를 쉽게 찾아 편집할 수 있음

- 자식 활동이 지속되지 않도록 하는 NoPersistScope 컨테이너 활동

- C# 식에 대한 지원

    - Visual Basic을 사용하는 워크플로 프로젝트에서는 Visual Basic 식을 사용하고, C# 워크플로 프로젝트에서는 C# 식을 사용합니다.

    - Visual Studio 2010에서 만들어지고 Visual Basic 식이 있는 C# 워크플로 프로젝트는 C# 식을 사용하는 C# 워크플로 프로젝트와 호환됩니다.

- 버전 관리 향상

    - 지속되는 워크플로 인스턴스와 해당 워크플로 정의 사이에 매핑을 제공하는 새로운 <xref:System.Activities.WorkflowIdentity> 클래스

    - <xref:System.ServiceModel.Activities.WorkflowServiceHost>를 비롯하여 동일한 호스트에서 여러 워크플로 버전을 Side-by-Side 실행

    - 동적 업데이트에서 지속된 워크플로 인스턴스의 정의를 수정할 수 있는 기능

- 기존 서비스 계약과 일치하도록 자동 생성 활동에 대한 지원을 제공하는 계약 중심 워크플로 서비스 개발

 자세한 내용은 [Windows Workflow Foundation의 새로운 기능](http://go.microsoft.com/fwlink/?LinkId=228176)을 참조하십시오.

<a name="tailored"></a> 
### [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)]
 [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 응용 프로그램은 특정 폼 팩터용으로 설계되었으며 Windows 운영 체제의 강력한 기능을 활용합니다. [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 또는 4.5.1의 하위 집합은 C# 또는 Visual Basic을 사용하여 Windows용 [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] 응용 프로그램을 빌드하는 데 사용할 수 있습니다. 이 하위 집합을 [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)]이라고 하며 Windows 개발자 센터의 [개요](http://go.microsoft.com/fwlink/?LinkId=228491)에 설명되어 있습니다.

<a name="portable"></a> 
### <a name="portable-class-libraries"></a>이식 가능한 클래스 라이브러리
 [!INCLUDE[vs_dev11_long](../../../includes/vs-dev11-long-md.md)] 및 이후 버전의 이식 가능한 클래스 라이브러리 프로젝트를 사용하여 여러 .NET Framework 플랫폼에서 작동하는 관리되는 어셈블리를 작성하고 빌드할 수 있습니다. 이식 가능한 클래스 라이브러리 프로젝트를 사용하여 대상 플랫폼(예: Windows Phone 및 [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)])을 선택합니다. 프로젝트에서 사용할 수 있는 형식 및 멤버는 이러한 플랫폼에서 공용 형식 및 멤버로 자동으로 제한됩니다. 자세한 내용은 [이식 가능한 클래스 라이브러리](../../../docs/standard/cross-platform/cross-platform-development-with-the-portable-class-library.md)를 참조하십시오.

## <a name="see-also"></a>참고 항목
 [.NET Framework 및 번외 릴리스](../../../docs/framework/get-started/the-net-framework-and-out-of-band-releases.md)   
 [Visual Studio 2017의 새로운 기능](/visualstudio/ide/whats-new-in-visual-studio)   
 [ASP.NET](/aspnet)   
 [Visual C++의 새로운 기능](/cpp/what-s-new-for-visual-cpp-in-visual-studio) 