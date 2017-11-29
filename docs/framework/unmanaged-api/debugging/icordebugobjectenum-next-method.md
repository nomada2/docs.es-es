---
title: "ICorDebugObjectEnum::Next (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugObjectEnum.Next
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugObjectEnum::Next
helpviewer_keywords:
- Next method, ICorDebugObjectEnum interface [.NET Framework debugging]
- ICorDebugObjectEnum::Next method [.NET Framework debugging]
ms.assetid: 10093e3d-26b6-4ad7-8ef3-bbf66243fc02
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 72195dbf74639d5799bb96754019dddf0f30101a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugobjectenumnext-method"></a><span data-ttu-id="a0185-102">ICorDebugObjectEnum::Next (Método)</span><span class="sxs-lookup"><span data-stu-id="a0185-102">ICorDebugObjectEnum::Next Method</span></span>
<span data-ttu-id="a0185-103">Obtiene las direcciones virtuales relativas (RVA) del número especificado de objetos de la enumeración, comenzando en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="a0185-103">Gets the relative virtual addresses (RVAs) of the specified number of objects from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0185-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0185-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]    
        CORDB_ADDRESS objects[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a0185-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0185-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="a0185-106">[in] Número de objetos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a0185-106">[in] The number of objects to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="a0185-107">[out] Una matriz de punteros, cada uno de los cuales apunta a un objeto CORDB_ADDRESS.</span><span class="sxs-lookup"><span data-stu-id="a0185-107">[out] An array of pointers, each of which points to a CORDB_ADDRESS object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="a0185-108">[out] Puntero al número de objetos realmente devueltos.</span><span class="sxs-lookup"><span data-stu-id="a0185-108">[out] Pointer to the number of objects actually returned.</span></span> <span data-ttu-id="a0185-109">Este valor puede ser null si `celt` es uno.</span><span class="sxs-lookup"><span data-stu-id="a0185-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0185-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0185-110">Requirements</span></span>  
 <span data-ttu-id="a0185-111">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a0185-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0185-112">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a0185-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a0185-113">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a0185-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a0185-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0185-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0185-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0185-115">See Also</span></span>  
 