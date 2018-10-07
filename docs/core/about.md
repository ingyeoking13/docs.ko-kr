---
title: .NET Core 정보
description: .NET Core에 대한 자세히 알아봅니다.
author: richlander
ms.author: mairaw
ms.date: 08/01/2018
ms.openlocfilehash: d9943246b683c8fd892e7bc5fd09a10b72e31a5f
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/23/2018
ms.locfileid: "48252227"
---
# <a name="about-net-core"></a><span data-ttu-id="b8825-103">.NET Core 정보</span><span class="sxs-lookup"><span data-stu-id="b8825-103">About .NET Core</span></span>

<span data-ttu-id="b8825-104">.NET Core에는 다음과 같은 특징이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-104">.NET Core has the following characteristics:</span></span>

- <span data-ttu-id="b8825-105">**플랫폼 간:** Windows, macOS 및 Linux [운영 체제](https://github.com/dotnet/core/blob/master/os-lifecycle-policy.md)에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-105">**Cross-platform:** Runs on Windows, macOS and Linux [operating systems](https://github.com/dotnet/core/blob/master/os-lifecycle-policy.md).</span></span>
- <span data-ttu-id="b8825-106">**아키텍처 간에 일관됨:** x64, x86 및 ARM을 비롯한 여러 아키텍처에서 동일한 동작을 사용하여 코드를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-106">**Consistent across architectures:** Runs your code with the same behavior on multiple architectures, including x64, x86, and ARM.</span></span>
- <span data-ttu-id="b8825-107">**명령줄 도구:** 로컬 개발 및 연속 통합 시나리오에서 사용된 사용하기 쉬운 명령줄 도구가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-107">**Command-line tools:**  Includes easy-to-use command-line tools that be used for local development and in continuous-integration scenarios.</span></span>
- <span data-ttu-id="b8825-108">**유연한 배포:** 앱이나 설치된 side-by-side사용자 또는 시스템 수준에 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-108">**Flexible deployment:** Can be included in your app or installed side-by-side user- or machine-wide.</span></span> <span data-ttu-id="b8825-109">[Docker 컨테이너](docker/index.md)에서 사용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-109">Can be used with [Docker containers](docker/index.md).</span></span>
- <span data-ttu-id="b8825-110">**호환 가능:** .NET Core는 [.NET Standard](../standard/net-standard.md)를 통해 .NET Framework, Xamarin 및 Mono와 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-110">**Compatible:** .NET Core is compatible with .NET Framework, Xamarin and Mono, via [.NET Standard](../standard/net-standard.md).</span></span>
- <span data-ttu-id="b8825-111">**오픈 소스:** .NET Core 플랫폼은 MIT 및 Apache 2 라이선스를 사용하는 오픈 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-111">**Open source:** The .NET Core platform is open source, using MIT and Apache 2 licenses.</span></span> <span data-ttu-id="b8825-112">.NET Core는 [.NET Foundation](https://dotnetfoundation.org/) 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-112">.NET Core is a [.NET Foundation](https://dotnetfoundation.org/) project.</span></span>
- <span data-ttu-id="b8825-113">**Microsoft에서 지원됨:** .NET Core는 [.NET Core 지원](https://www.microsoft.com/net/core/support/)에 따라 Microsoft에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-113">**Supported by Microsoft:** .NET Core is supported by Microsoft, per [.NET Core Support](https://www.microsoft.com/net/core/support/).</span></span>

## <a name="languages"></a><span data-ttu-id="b8825-114">언어</span><span class="sxs-lookup"><span data-stu-id="b8825-114">Languages</span></span>

<span data-ttu-id="b8825-115">C#, Visual Basic 및 F# 언어를 사용하여 .NET Core에 대한 응용 프로그램 및 라이브러리를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-115">C#, Visual Basic, and F# languages can be used to write applications and libraries for .NET Core.</span></span> <span data-ttu-id="b8825-116">이러한 언어는 [Visual Studio](https://visualstudio.microsoft.com/vs/), [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp), Sublime Text 및 Vim을 비롯한 즐겨찾는 텍스트 편집기 및 IDE에 통합될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-116">These languages are or can be integrated into your favorite text editors and IDEs, including [Visual Studio](https://visualstudio.microsoft.com/vs/), [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp), Sublime Text and Vim.</span></span> <span data-ttu-id="b8825-117">이 통합은 [OmniSharp](http://www.omnisharp.net/) 및 [Ionide](http://ionide.io) 프로젝트의 적합한 담당자에 의해 부분적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-117">This integration is provided, in part, by the good folks from the [OmniSharp](http://www.omnisharp.net/) and [Ionide](http://ionide.io) projects.</span></span>

## <a name="apis"></a><span data-ttu-id="b8825-118">API</span><span class="sxs-lookup"><span data-stu-id="b8825-118">APIs</span></span>

<span data-ttu-id="b8825-119">.NET Core는 다음과 같은 여러 시나리오에서 API를 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-119">.NET Core exposes APIs for many scenarios, a few of which follow:</span></span>

- <span data-ttu-id="b8825-120">[bool][bool] 및 [int][int]와 같은 기본 형식</span><span class="sxs-lookup"><span data-stu-id="b8825-120">Primitive types, such as [bool][bool] and [int][int].</span></span>
- <span data-ttu-id="b8825-121"><xref:System.Collections.Generic.List%601?displayProperty=nameWithType> 및 <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType>과 같은 컬렉션</span><span class="sxs-lookup"><span data-stu-id="b8825-121">Collections, such as <xref:System.Collections.Generic.List%601?displayProperty=nameWithType> and <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType>.</span></span>
- <span data-ttu-id="b8825-122"><xref:System.Net.Http.HttpClient?displayProperty=nameWithType> 및 <xref:System.IO.FileStream?displayProperty=nameWithType>과 같은 유틸리티 형식</span><span class="sxs-lookup"><span data-stu-id="b8825-122">Utility types, such as <xref:System.Net.Http.HttpClient?displayProperty=nameWithType>, and <xref:System.IO.FileStream?displayProperty=nameWithType>.</span></span>
- <span data-ttu-id="b8825-123"><xref:System.Data.DataSet?displayProperty=nameWithType> 및 [DbSet][dbset]과 같은 데이터 형식</span><span class="sxs-lookup"><span data-stu-id="b8825-123">Data types, such as <xref:System.Data.DataSet?displayProperty=nameWithType>, and [DbSet][dbset].</span></span>
- <span data-ttu-id="b8825-124"><xref:System.Numerics.Vector?displayProperty=nameWithType> 및 [파이프라인][pipelines]과 같은 고성능 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-124">High performance types, such as <xref:System.Numerics.Vector?displayProperty=nameWithType> and [Pipelines][pipelines].</span></span>

<span data-ttu-id="b8825-125">.NET Core는 [.NET Standard](../standard/net-standard.md) 사양을 구현하여 .NET Framework 및 Mono API에서 호환성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-125">.NET Core provides compatibility with .NET Framework and Mono APIs by implementing the [.NET Standard](../standard/net-standard.md) specification.</span></span>

[bool]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/bool
[int]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/int
[pipelines]: https://blogs.msdn.microsoft.com/dotnet/2018/07/09/system-io-pipelines-high-performance-io-in-net/
[dbset]: https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/

## <a name="frameworks"></a><span data-ttu-id="b8825-126">프레임워크</span><span class="sxs-lookup"><span data-stu-id="b8825-126">Frameworks</span></span>

<span data-ttu-id="b8825-127">여러 프레임워크가 .NET Core를 기반으로 빌드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-127">Multiple frameworks have been built on top of .NET Core:</span></span>

- [<span data-ttu-id="b8825-128">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="b8825-128">ASP.NET Core</span></span>](/aspnet/core/)
- [<span data-ttu-id="b8825-129">Windows 10 UWP(유니버설 Windows 플랫폼)</span><span class="sxs-lookup"><span data-stu-id="b8825-129">Windows 10 Universal Windows Platform (UWP)</span></span>](https://developer.microsoft.com/windows)
- [<span data-ttu-id="b8825-130">Tizen</span><span class="sxs-lookup"><span data-stu-id="b8825-130">Tizen</span></span>](https://developer.tizen.org/development/training/.net-application)

## <a name="composition"></a><span data-ttu-id="b8825-131">컴퍼지션</span><span class="sxs-lookup"><span data-stu-id="b8825-131">Composition</span></span>

<span data-ttu-id="b8825-132">.NET Core는 다음과 같은 부분으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-132">.NET Core is composed of the following parts:</span></span>

- <span data-ttu-id="b8825-133">[.NET Core 런타임](https://github.com/dotnet/coreclr)은 형식 시스템, 어셈블리 로드, 가비지 수집기, 네이티브 interop 및 기타 기본 서비스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-133">The [.NET Core runtime](https://github.com/dotnet/coreclr), which provides a type system, assembly loading, a garbage collector, native interop and other basic services.</span></span> <span data-ttu-id="b8825-134">[.NET Core 프레임워크 라이브러리](https://github.com/dotnet/corefx)는 기본 데이터 형식, 앱 구성 형식 및 기본 유틸리티를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-134">[.NET Core framework libraries](https://github.com/dotnet/corefx) provide primitive data types, app composition types and fundamental utilities.</span></span>
- <span data-ttu-id="b8825-135">[ASP.NET 런타임](https://github.com/aspnet/home)은 웹앱, IoT 앱 및 모바일 백 엔드와 같이 최신 클라우드 기반 인터넷 연결 응용 프로그램을 빌드하는 프레임워크를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-135">The [ASP.NET runtime](https://github.com/aspnet/home), which provides a framework for building modern cloud based internet connected applications, such as web apps, IoT apps and mobile backends.</span></span>
- <span data-ttu-id="b8825-136">.NET Core 개발자 환경을 사용할 수 있도록 하는 [.NET Core CLI 도구](https://github.com/dotnet/cli) 및 언어 컴파일러([Roslyn](https://github.com/dotnet/roslyn) 및 [F#](https://github.com/microsoft/visualfsharp))입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-136">The [.NET Core CLI tools](https://github.com/dotnet/cli) and language compilers ([Roslyn](https://github.com/dotnet/roslyn) and [F#](https://github.com/microsoft/visualfsharp)) that enable the .NET Core developer experience.</span></span>
- <span data-ttu-id="b8825-137">[dotnet 도구](https://github.com/dotnet/core-setup)는 .NET Core 앱 및 CLI 도구를 시작하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-137">The [dotnet tool](https://github.com/dotnet/core-setup), which is used to launch .NET Core apps and CLI tools.</span></span> <span data-ttu-id="b8825-138">이 호스트는 런타임을 선택하고 런타임을 호스트하며 어셈블리 로드 정책을 제공하고 앱 및 도구를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-138">It selects the runtime and hosts the runtime, provides an assembly loading policy and launches apps and tools.</span></span>

<span data-ttu-id="b8825-139">이러한 구성 요소는 다음과 같은 방법으로 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-139">These components are distributed in the following ways:</span></span>

- <span data-ttu-id="b8825-140">[.NET Core 런타임](https://www.microsoft.com/net/download/dotnet-core/2.1) - .NET Core 런타임 및 프레임워크 라이브러리가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-140">[.NET Core Runtime](https://www.microsoft.com/net/download/dotnet-core/2.1) -- includes the .NET Core runtime and framework libraries.</span></span>
- <span data-ttu-id="b8825-141">[ASP.NET Core 런타임](https://www.microsoft.com/net/download/dotnet-core/2.1) - ASP.NET Core 및 .NET Core 런타임 및 프레임워크 라이브러리가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-141">[ASP.NET Core Runtime](https://www.microsoft.com/net/download/dotnet-core/2.1) -- includes ASP.NET Core and .NET Core runtime and framework libraries.</span></span>
- <span data-ttu-id="b8825-142">[.NET Core SDK](https://www.microsoft.com/net/download/dotnet-core/2.1) - .NET CLI 도구, ASP.NET Core 런타임 및 .NET Core 런타임 및 프레임워크가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-142">[.NET Core SDK](https://www.microsoft.com/net/download/dotnet-core/2.1) -- includes the .NET CLI Tools, ASP.NET Core runtime, and .NET Core runtime and framework.</span></span>

### <a name="open-source"></a><span data-ttu-id="b8825-143">오픈 소스</span><span class="sxs-lookup"><span data-stu-id="b8825-143">Open Source</span></span>

<span data-ttu-id="b8825-144">[.NET Core](https://github.com/dotnet/core)는 오픈 소스([MIT 라이선스](https://github.com/dotnet/core/blob/master/LICENSE.TXT))이며 2014년 Microsoft에 의해 [.NET Foundation](https://dotnetfoundation.org)에 제공되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-144">[.NET Core](https://github.com/dotnet/core) is open source ([MIT license](https://github.com/dotnet/core/blob/master/LICENSE.TXT)) and was contributed to the [.NET Foundation](https://dotnetfoundation.org) by Microsoft in 2014.</span></span> <span data-ttu-id="b8825-145">이제 가장 많이 사용되는 .NET Foundation 프로젝트 중의 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-145">It is now one of the most active .NET Foundation projects.</span></span> <span data-ttu-id="b8825-146">이 프로젝트는 개인, 교육 또는 상업용으로 개인 및 회사에서 자유롭게 채택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-146">It can be freely adopted by individuals and companies, including for personal, academic or commercial purposes.</span></span> <span data-ttu-id="b8825-147">여러 회사에서 앱, 도구, 새 플랫폼 및 호스팅 서비스의 일부로 .NET Core를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-147">Multiple companies use .NET Core as part of apps, tools, new platforms and hosting services.</span></span> <span data-ttu-id="b8825-148">이러한 회사 중 일부는 GitHub에서 .NET Core에 대한 중요한 정보를 제공하고 [.NET Foundation Technical Steering Group(.NET Foundation 기술 방향 설정 그룹)](https://dotnetfoundation.org/blog/tsg-welcome)의 일부로 제품 판매에 대한 지침을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-148">Some of these companies make significant contributions to .NET Core on GitHub and provide guidance on the product direction as part of the [.NET Foundation Technical Steering Group](https://dotnetfoundation.org/blog/tsg-welcome).</span></span>

### <a name="designed-for-adaptability"></a><span data-ttu-id="b8825-149">뛰어난 적응성</span><span class="sxs-lookup"><span data-stu-id="b8825-149">Designed for Adaptability</span></span>

<span data-ttu-id="b8825-150">.NET Core는 다른 .NET 제품에 비해 매우 유사하지만 고유한 제품으로 구축되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-150">.NET Core has been built as a very similar but unique product relative to other .NET products.</span></span> <span data-ttu-id="b8825-151">.NET Core는 새 플랫폼 및 워크로드에 광범위하게 적응되도록 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-151">It has been designed to enable broad adaptability to new platforms and workloads.</span></span> <span data-ttu-id="b8825-152">여러 개의 OS 및 CPU 포트가 지원되며 훨씬 더 많은 포트로 이식할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-152">It has several OS and CPU ports available and may be ported to many more.</span></span>

<span data-ttu-id="b8825-153">제품은 여러 조각으로 구분되어 다양한 시점에 다양한 부품을 새 플랫폼에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-153">The product is broken into several pieces, enabling the various parts to be adapted to new platforms at different times.</span></span> <span data-ttu-id="b8825-154">런타임 및 플랫폼별 기본 라이브러리는 하나의 단위로 이식해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-154">The runtime and platform-specific foundational libraries must be ported as a unit.</span></span> <span data-ttu-id="b8825-155">플랫폼 제약 없는 라이브러리는 구성에 따라 모든 플랫폼에서 있는 그대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-155">Platform-agnostic libraries should work as-is on all platforms, by construction.</span></span> <span data-ttu-id="b8825-156">플랫폼별 구현을 줄여 개발자 효율성을 향상시키거나, 알고리즘이나 API를 전체 또는 일부로 구현할 수 있을 때마다 플랫폼 중립적인 C# 코드를 선호한다는 등 프로젝트에 대한 편견이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-156">There is a project bias to reducing platform-specific implementations to increase developer efficiency, preferring platform-neutral C# code whenever an algorithm or API can be implemented in-full or in-part that way.</span></span>

<span data-ttu-id="b8825-157">일반적으로 사용자는 여러 운영 체제를 지원하기 위해 .NET Core를 구현하는 방법을 질문합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-157">People commonly ask how .NET Core is implemented in order to support multiple operating systems.</span></span> <span data-ttu-id="b8825-158">또한 별도의 구현이 있는지 또는 [조건부 컴파일](https://en.wikipedia.org/wiki/Conditional_compilation)이 사용되는지에 대해서도 질문합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-158">They typically ask if there are separate implementations or if [conditional compilation](https://en.wikipedia.org/wiki/Conditional_compilation) is used.</span></span> <span data-ttu-id="b8825-159">둘 다 조건부 컴파일에 대한 강력한 편견이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-159">It's both, with a strong bias towards conditional compilation.</span></span>

<span data-ttu-id="b8825-160">대부분의 [CoreFX](https://github.com/dotnet/corefx)가 모든 플랫폼에서 공유되는 플랫폼 중립 코드임을 다음 차트에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-160">You can see in the chart below that the vast majority of [CoreFX](https://github.com/dotnet/corefx) is platform-neutral code that is shared across all platforms.</span></span> <span data-ttu-id="b8825-161">플랫폼 중립 코드는 모든 플랫폼에서 사용할 수 있는 이식 가능한 단일 어셈블리로 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-161">Platform-neutral code can be implemented as a single portable assembly that is used on all platforms.</span></span>

![CoreFX: 플랫폼별 코드 줄](../images/corefx-platforms-loc.png)

<span data-ttu-id="b8825-163">Windows 및 Unix 구현은 크기가 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-163">Windows and Unix implementations are similar in size.</span></span> <span data-ttu-id="b8825-164">CoreFX는 [Microsoft.Win32.Registry](https://github.com/dotnet/corefx/tree/master/src/Microsoft.Win32.Registry)와 같은 일부 Windows 전용 기능을 구현하지만 여러 Unix 전용 개념은 구현하지 않기 때문에 Windows 구현이 더 큽니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-164">Windows has a larger implementation since CoreFX implements some Windows-only features, such as [Microsoft.Win32.Registry](https://github.com/dotnet/corefx/tree/master/src/Microsoft.Win32.Registry) but does not yet implement many Unix-only concepts.</span></span> <span data-ttu-id="b8825-165">또한 대부분의 Linux 및 macOS 구현이 Unix 구현에서 공유되는데 Linux 및 macOS 관련 구현의 크기가 거의 비슷함을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-165">You will also see that the majority of the Linux and macOS implementations are shared across a Unix implementation, while the Linux- and macOS-specific implementations are roughly similar in size.</span></span>

<span data-ttu-id="b8825-166">.NET Core에는 플랫폼별 라이브러리와 플랫폼 중립 라이브러리가 혼합되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-166">There are a mix of platform-specific and platform-neutral libraries in .NET Core.</span></span> <span data-ttu-id="b8825-167">몇 가지 예제에서 패턴을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-167">You can see the pattern in a few examples:</span></span>

- <span data-ttu-id="b8825-168">[CoreCLR](https://github.com/dotnet/coreclr)는 플랫폼별이며,</span><span class="sxs-lookup"><span data-stu-id="b8825-168">[CoreCLR](https://github.com/dotnet/coreclr) is platform-specific.</span></span> <span data-ttu-id="b8825-169">메모리 관리자 및 스레드 스케줄러와 같은 OS 하위 시스템을 기반으로 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-169">It builds on top of OS subsystems, like the memory manager and thread scheduler.</span></span>
- <span data-ttu-id="b8825-170">저장소 및 암호화 API가 각 OS에서 다르기 때문에 [System.IO](https://github.com/dotnet/corefx/tree/master/src/System.IO) 및 [System.Security.Cryptography.Algorithms](https://github.com/dotnet/corefx/tree/master/src/System.Security.Cryptography.Algorithms)는 플랫폼별입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-170">[System.IO](https://github.com/dotnet/corefx/tree/master/src/System.IO) and [System.Security.Cryptography.Algorithms](https://github.com/dotnet/corefx/tree/master/src/System.Security.Cryptography.Algorithms) are platform-specific, given that storage and cryptography APIs are different on each OS.</span></span>
- <span data-ttu-id="b8825-171">[System.Collections](https://github.com/dotnet/corefx/tree/master/src/System.Collections) 및 [System.Linq](https://github.com/dotnet/corefx/tree/master/src/System.Linq)는 데이터 구조를 통해 만들고 작동하기 때문에 플랫폼 중립입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-171">[System.Collections](https://github.com/dotnet/corefx/tree/master/src/System.Collections) and [System.Linq](https://github.com/dotnet/corefx/tree/master/src/System.Linq) are platform-neutral, given that they create and operate over data structures.</span></span>

## <a name="comparisons-to-other-net-implementations"></a><span data-ttu-id="b8825-172">다른 .NET 구현과 비교</span><span class="sxs-lookup"><span data-stu-id="b8825-172">Comparisons to other .NET implementations</span></span>

<span data-ttu-id="b8825-173">기존 .NET 구현과 비교하여 .NET Core의 크기 및 모양을 이해하는 것이 가장 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-173">It is perhaps easiest to understand the size and shape of .NET Core by comparing it to existing .NET implementations.</span></span>

### <a name="comparison-with-net-framework"></a><span data-ttu-id="b8825-174">.NET Framework와 비교</span><span class="sxs-lookup"><span data-stu-id="b8825-174">Comparison with .NET Framework</span></span>

<span data-ttu-id="b8825-175">.NET은 Microsoft가 2000년에 처음 발표한 후 발전해 왔습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-175">.NET was first announced by Microsoft in 2000 and then evolved from there.</span></span> <span data-ttu-id="b8825-176">.NET Framework는 Microsoft에서 거의 20년 가까이 만들어낸 기본 .NET 구현입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-176">The .NET Framework has been the primary .NET implementation produced by Microsoft during that nearly two decade period.</span></span>

<span data-ttu-id="b8825-177">.NET Core와 .NET Framework 간의 주요 차이점은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-177">The major differences between .NET Core and the .NET Framework:</span></span>

- <span data-ttu-id="b8825-178">**앱 모델** - .NET Core는 일부 .NET Framework 앱 모델을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-178">**App-models** -- .NET Core does not support all the .NET Framework app-models.</span></span> <span data-ttu-id="b8825-179">특히, ASP.NET Web Forms 및 MVC를 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-179">In particular, it doesn't support ASP.NET Web Forms and MVC.</span></span> <span data-ttu-id="b8825-180">[.NET Core 3이 WPF 및 Windows Forms를 지원한다](https://blogs.msdn.microsoft.com/dotnet/2018/05/07/net-core-3-and-support-for-windows-desktop-applications/)고 발표했습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-180">It was announced that [.NET Core 3 will support WPF and Windows Forms](https://blogs.msdn.microsoft.com/dotnet/2018/05/07/net-core-3-and-support-for-windows-desktop-applications/).</span></span>
- <span data-ttu-id="b8825-181">**API** - .NET Core에는 팩터링이 다른 .NET Framework 기본 클래스 라이브러리의 대량 하위 집합이 포함됩니다(핵심 사례에서 어셈블리 이름이 다르고, 형식에서 노출된 멤버가 다름).</span><span class="sxs-lookup"><span data-stu-id="b8825-181">**APIs** -- .NET Core contains a large subset of .NET Framework Base Class Library, with a different factoring (assembly names are different; members exposed on types differ in key cases).</span></span> <span data-ttu-id="b8825-182">이러한 차이로 인해 어떤 경우 .NET Core에 대한 포트 원본을 변경해야 합니다([microsoft/dotnet-apiport](https://github.com/microsoft/dotnet-apiport) 참조).</span><span class="sxs-lookup"><span data-stu-id="b8825-182">These differences require changes to port source to .NET Core in some cases (see [microsoft/dotnet-apiport](https://github.com/microsoft/dotnet-apiport)).</span></span> <span data-ttu-id="b8825-183">.NET Core는 [.NET Standard](../standard/net-standard.md) API 사양을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-183">.NET Core implements the [.NET Standard](../standard/net-standard.md) API specification.</span></span>
- <span data-ttu-id="b8825-184">**하위 시스템** -- .Net Core는 더 간단한 구현 및 프로그래밍 모델 구축을 위해 .NET Framework에 하위 시스템의 하위 집합을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-184">**Subsystems** -- .NET Core implements a subset of the subsystems in the .NET Framework, with the goal of a simpler implementation and programming model.</span></span> <span data-ttu-id="b8825-185">예를 들어 CAS(코드 액세스 보안)는 지원되지 않지만 리플렉션은 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-185">For example, Code Access Security (CAS) is not supported, while reflection is supported.</span></span>
- <span data-ttu-id="b8825-186">**플랫폼** -- .NET Framework는 Windows와 Windows Server를 지원하는 반면 .NET Core는 macOS 및 Linux도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-186">**Platforms** -- The .NET Framework supports Windows and Windows Server while .NET Core also supports macOS and Linux.</span></span>
- <span data-ttu-id="b8825-187">**오픈 소스** -- .NET Core는 오픈 소스이며, [.NET Framework의 읽기 전용 하위 집합](https://github.com/microsoft/referencesource)은 오픈 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-187">**Open Source** -- .NET Core is open source, while a [read-only subset of the .NET Framework](https://github.com/microsoft/referencesource) is open source.</span></span>

<span data-ttu-id="b8825-188">.NET Core는 고유하며, .NET Framework 및 기타 .NET 구현과 현저한 차이가 있지만, 원본 또는 이진 공유 기술을 사용하여 이러한 구현 간에 간단하게 코드를 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-188">While .NET Core is unique and has significant differences to the .NET Framework and other .NET implementations, it is straightforward to share code between these implementations, using either source or binary sharing techniques.</span></span>

### <a name="comparison-with-mono"></a><span data-ttu-id="b8825-189">Mono와 비교</span><span class="sxs-lookup"><span data-stu-id="b8825-189">Comparison with Mono</span></span>

<span data-ttu-id="b8825-190">[Mono](http://www.mono-project.com/)는 원래 플랫폼 간 [오픈 소스](https://github.com/mono/mono) .NET 구현으로, 2004년에 처음 제공되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-190">[Mono](http://www.mono-project.com/) is the original cross-platform and [open source](https://github.com/mono/mono) .NET implementation, first shipping in 2004.</span></span> <span data-ttu-id="b8825-191">.NET Framework의 커뮤니티 복제본으로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-191">It can be thought of as a community clone of the .NET Framework.</span></span> <span data-ttu-id="b8825-192">Mono 프로젝트 팀은 호환되는 구현을 제공하기 위해 Microsoft에서 게시한 오픈 [.NET 표준](https://github.com/dotnet/coreclr/blob/master/Documentation/project-docs/dotnet-standards.md)(특히 ECMA 335)을 사용했습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-192">The Mono project team relied on the open [.NET standards](https://github.com/dotnet/coreclr/blob/master/Documentation/project-docs/dotnet-standards.md) (notably ECMA 335) published by Microsoft in order to provide a compatible implementation.</span></span>

<span data-ttu-id="b8825-193">.NET Core와 Mono 간의 주요 차이점은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-193">The major differences between .NET Core and Mono:</span></span>

- <span data-ttu-id="b8825-194">**앱 모델** -- Mono는 Xamarin 제품을 통해 .NET Framework 앱 모델의 하위 집합(예: Windows Forms) 및 몇 가지 추가 모델(예: [Xamarin.iOS](https://www.xamarin.com/platform))을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-194">**App-models** -- Mono supports a subset of the .NET Framework app-models (for example, Windows Forms) and some additional ones (for example, [Xamarin.iOS](https://www.xamarin.com/platform)) through the Xamarin product.</span></span> <span data-ttu-id="b8825-195">.NET Core는 이러한 모델을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-195">.NET Core doesn't support these.</span></span>
- <span data-ttu-id="b8825-196">**API** -- Mono는 .NET Framework API의 [큰 하위 집합](http://docs.go-mono.com/?link=root%3a%2fclasslib)을 지원하며, 동일한 어셈블리 이름 및 팩터링을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-196">**APIs** -- Mono supports a [large subset](http://docs.go-mono.com/?link=root%3a%2fclasslib) of the .NET Framework APIs, using the same assembly names and factoring.</span></span>
- <span data-ttu-id="b8825-197">**플랫폼** -- Mono는 여러 플랫폼 및 CPU를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-197">**Platforms** -- Mono supports many platforms and CPUs.</span></span>
- <span data-ttu-id="b8825-198">**오픈 소스** -- Mono와 .NET Core 둘 다 MIT 라이선스를 사용하며 .NET Foundation 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-198">**Open Source** -- Mono and .NET Core both use the MIT license and are .NET Foundation projects.</span></span>
- <span data-ttu-id="b8825-199">**포커스** -- 최근 몇 년 간 Mono의 주요 포커스는 모바일 플랫폼인 반면, .NET Core의 포커스는 클라우드 및 데스크톱 워크로드입니다.</span><span class="sxs-lookup"><span data-stu-id="b8825-199">**Focus** -- The primary focus of Mono in recent years is mobile platforms, while .NET Core is focused on cloud and desktop workloads.</span></span>