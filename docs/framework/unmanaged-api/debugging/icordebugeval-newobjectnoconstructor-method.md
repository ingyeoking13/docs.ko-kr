---
title: "ICorDebugEval::NewObjectNoConstructor 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugEval.NewObjectNoConstructor
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugEval::NewObjectNoConstructor
helpviewer_keywords:
- NewObjectNoConstructor method [.NET Framework debugging]
- ICorDebugEval::NewObjectNoConstructor method [.NET Framework debugging]
ms.assetid: 80d509ca-b5e3-4c46-9c14-800db73d9bf7
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 415c8f2faae44fbdfec5441abaff8b93042ac124
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugevalnewobjectnoconstructor-method"></a><span data-ttu-id="06cfa-102">ICorDebugEval::NewObjectNoConstructor 메서드</span><span class="sxs-lookup"><span data-stu-id="06cfa-102">ICorDebugEval::NewObjectNoConstructor Method</span></span>
<span data-ttu-id="06cfa-103">생성자 메서드를 호출 하지 않고 지정 된 형식의 새 개체 인스턴스를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cfa-103">Allocates a new object instance of the specified type, without attempting to call a constructor method.</span></span>  
  
 <span data-ttu-id="06cfa-104">이 메서드는.NET Framework 버전 2.0에서에서 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06cfa-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="06cfa-105">사용 하 여 [icordebugeval2:: Newparameterizedobjectnoconstructor](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md) 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cfa-105">Use [ICorDebugEval2::NewParameterizedObjectNoConstructor](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06cfa-106">구문</span><span class="sxs-lookup"><span data-stu-id="06cfa-106">Syntax</span></span>  
  
```  
HRESULT NewObjectNoConstructor (  
    [in] ICorDebugClass     *pClass  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="06cfa-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="06cfa-107">Parameters</span></span>  
 `pClass`  
 <span data-ttu-id="06cfa-108">[in] 인스턴스화할 수 있는 개체의 유형을 나타내는 ICorDebugClass 개체에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="06cfa-108">[in] Pointer to an ICorDebugClass object that represents the type of object to be instantiated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06cfa-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="06cfa-109">Requirements</span></span>  
 <span data-ttu-id="06cfa-110">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="06cfa-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06cfa-111">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="06cfa-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="06cfa-112">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="06cfa-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="06cfa-113">**.NET framework 버전:** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="06cfa-113">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06cfa-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="06cfa-114">See Also</span></span>  
 [<span data-ttu-id="06cfa-115">NewParameterizedObjectNoConstructor 메서드</span><span class="sxs-lookup"><span data-stu-id="06cfa-115">NewParameterizedObjectNoConstructor Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md)