---
title: 오픈 소스 라이브러리 지침
description: 고품질 .NET 라이브러리를 만드는 개발자를 위한 모범 사례 권장 사항입니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 50fb745f7eb65abcaca76cebaf9991c48f559e59
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374914"
---
# <a name="open-source-library-guidance"></a><span data-ttu-id="72bbb-103">오픈 소스 라이브러리 지침</span><span class="sxs-lookup"><span data-stu-id="72bbb-103">Open-source library guidance</span></span>

<span data-ttu-id="72bbb-104">이 지침에서는 고품질 .NET 라이브러리를 만드는 개발자를 위한 권장 사항을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-104">This guidance provides recommendations for developers to create high-quality .NET libraries.</span></span> <span data-ttu-id="72bbb-105">이 설명서는 .NET 라이브러리를 빌드하는 경우 *방법*이 아닌 *내용* 및 *이유*에 중점을 둡니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-105">This documentation focuses on the *what* and the *why* when building a .NET library, not the *how*.</span></span>

<span data-ttu-id="72bbb-106">고품질 오픈 소스 .NET 라이브러리의 측면:</span><span class="sxs-lookup"><span data-stu-id="72bbb-106">Aspects of high-quality open-source .NET libraries:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="72bbb-107">**포괄적** - 우수한 .NET 라이브러리는 여러 플랫폼 및 응용 프로그램을 지원하기 위해 노력합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-107">**Inclusive** - Good .NET libraries strive to support many platforms and applications.</span></span>
> * <span data-ttu-id="72bbb-108">**안정적** - 우수한 .NET 라이브러리는 에코시스템에서 공존하며 다양한 라이브러리를 사용하여 빌드된 응용 프로그램에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-108">**Stable** - Good .NET libraries coexist in the .NET ecosystem, running in applications built with many libraries.</span></span>
> * <span data-ttu-id="72bbb-109">**진화하도록 설계** - .NET 라이브러리는 시간이 지남에 따라 개선되고 진화하는 동시에 기존 사용자를 지원해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-109">**Designed to evolve** - .NET libraries should improve and evolve over time, while supporting existing users.</span></span>
> * <span data-ttu-id="72bbb-110">**디버깅 가능** - .NET 라이브러리는 사용자에 대해 뛰어난 디버깅 환경을 만드는 최신 도구를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-110">**Debuggable** - .NET libraries should use the latest tools to create a great debugging experience for users.</span></span>
> * <span data-ttu-id="72bbb-111">**신뢰할 수 있음** - .NET 라이브러리는 보안 모범 사례를 사용하는 NuGet에 게시하여 개발자의 신뢰를 얻고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-111">**Trusted** - .NET libraries have developers' trust by publishing to NuGet using security best practices.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="72bbb-112">시작</span><span class="sxs-lookup"><span data-stu-id="72bbb-112">Get Started</span></span>](./get-started.md)

## <a name="recommendations"></a><span data-ttu-id="72bbb-113">권장 사항</span><span class="sxs-lookup"><span data-stu-id="72bbb-113">Recommendations</span></span>

<span data-ttu-id="72bbb-114">각 문서에는 **수행**, **고려**, **회피** 및 **금지** 항목을 사용하는 .NET 라이브러리에 대한 권장 사항 목록이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-114">With each article, there is a list of recommendations for your .NET library using **Do**, **Consider**, **Avoid**, and **Do not**.</span></span> <span data-ttu-id="72bbb-115">각 권장 사항의 단어는 수행해야 하는 정도를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-115">The wording of each recommendation indicates how strongly it should be followed.</span></span>

<span data-ttu-id="72bbb-116">**수행** 권장 사항은 거의 항상 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-116">A **Do** recommendation is one that should almost always be followed:</span></span>

<span data-ttu-id="72bbb-117">**✔️ 수행** NuGet 패키지를 사용하여 라이브러리를 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-117">**✔️ DO** distribute your library using a NuGet package.</span></span>

<span data-ttu-id="72bbb-118">한편으로 **고려** 권장 사항은 일반적으로 따라야 하지만 규칙에 대한 정당한 예외가 있거나 지침을 따르지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-118">On the other hand, **Consider** recommendations should generally be followed, but there are legitimate exceptions to the rule and you shouldn't feel bad about not following the guidance:</span></span>

<span data-ttu-id="72bbb-119">**✔️ 고려** [SemVer 2.0.0](https://semver.org/)을 사용하여 NuGet 패키지 버전을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-119">**✔️ CONSIDER** using [SemVer 2.0.0](https://semver.org/) to version your NuGet package.</span></span>

<span data-ttu-id="72bbb-120">**회피** 권장 사항은 일반적으로 좋은 항목이지만 규칙을 깨는 것이 적합한 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-120">**Avoid** recommendations are things that are generally not a good idea, but breaking the rule sometimes makes sense:</span></span>

<span data-ttu-id="72bbb-121">**❌ 회피** 정확한 버전을 요구하는 NuGet 패키지 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-121">**❌ AVOID** NuGet package references that demand an exact version.</span></span>

<span data-ttu-id="72bbb-122">마지막으로, **금지**는 작업을 수행하지 않아야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-122">And finally, **do not** indicates something you should almost never do:</span></span>

<span data-ttu-id="72bbb-123">**❌ 금지** 강력한 이름이 지정되고 강력하지 않은 이름이 지정된 버전의 라이브러리를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-123">**❌ DO NOT** publish strong-named and non-strong-named versions of your library.</span></span> <span data-ttu-id="72bbb-124">예를 들어 `Contoso.Api` 및 `Contoso.Api.StrongNamed`를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="72bbb-124">For example, `Contoso.Api` and `Contoso.Api.StrongNamed`.</span></span>

>[!div class="step-by-step"]
[<span data-ttu-id="72bbb-125">다음</span><span class="sxs-lookup"><span data-stu-id="72bbb-125">Next</span></span>](./get-started.md)