---
title: "ICorDebugVariableSymbol::SetValue 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 4609418d-71fa-44bc-9618-4d529d25cabb
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 12c13259d20301b0f485a6041fa884b0996cbbdc
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvariablesymbolsetvalue-method"></a><span data-ttu-id="0ad9d-102">ICorDebugVariableSymbol::SetValue 메서드</span><span class="sxs-lookup"><span data-stu-id="0ad9d-102">ICorDebugVariableSymbol::SetValue Method</span></span>
<span data-ttu-id="0ad9d-103">바이트 배열의 값을 변수에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-103">Assigns the value of a byte array to a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ad9d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ad9d-104">Syntax</span></span>  
  
```  
HRESULT SetValue(  
   [in] ULONG32 offset,  
   [in] DWORD threadID,  
   [in] ULONG32 cbContext,  
   [in, size_is(cbContext)] BYTE context[],  
   [in] ULONG32 cbValue,  
   [in, size_is(cbValue)] BYTE pValue[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0ad9d-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ad9d-105">Parameters</span></span>  
 `offset`  
 <span data-ttu-id="0ad9d-106">[in] 값을 설정할 변수의 시작 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-106">[in] The starting offset in the variable at which to set the value.</span></span> <span data-ttu-id="0ad9d-107">이 매개 변수는 개체의 멤버 필드에 쓸 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-107">This parameter is used when writing to member fields in an object.</span></span>  
  
 `threadID`  
 <span data-ttu-id="0ad9d-108">[in] 새 값을 반영하도록 컨텍스트를 업데이트해야 하는 스레드의 스레드 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-108">[in] The thread identifier of the thread whose context must be updated to reflect the new value.</span></span>  
  
 `cbContext`  
 <span data-ttu-id="0ad9d-109">[in] 스레드 컨텍스트의 크기(바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-109">[in] The size in bytes of the thread context.</span></span>  
  
 `context`  
 <span data-ttu-id="0ad9d-110">[in] 값을 쓰는 데 사용되는 스레드 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-110">[in] The thread context used to write the value.</span></span>  
  
 `cbValue`  
 <span data-ttu-id="0ad9d-111">[in] `pValue` 버퍼의 크기(바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-111">[in] The size in bytes of the `pValue` buffer.</span></span>  
  
 `pValue`  
 <span data-ttu-id="0ad9d-112">[in] 설정할 값이 들어 있는 버퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-112">[in] The buffer that contains the value to set.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0ad9d-113">설명</span><span class="sxs-lookup"><span data-stu-id="0ad9d-113">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0ad9d-114">이 메서드는 .NET 네이티브에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-114">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ad9d-115">요구 사항</span><span class="sxs-lookup"><span data-stu-id="0ad9d-115">Requirements</span></span>  
 <span data-ttu-id="0ad9d-116">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad9d-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ad9d-117">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0ad9d-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0ad9d-118">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0ad9d-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0ad9d-119">**.NET framework 버전:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ad9d-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ad9d-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0ad9d-120">See Also</span></span>  
 [<span data-ttu-id="0ad9d-121">ICorDebugVariableSymbol 인터페이스</span><span class="sxs-lookup"><span data-stu-id="0ad9d-121">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)  
 [<span data-ttu-id="0ad9d-122">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="0ad9d-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)