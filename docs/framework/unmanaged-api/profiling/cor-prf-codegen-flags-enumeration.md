---
title: "COR_PRF_CODEGEN_FLAGS (Enumeración)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_CODEGEN_FLAGS
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_CODEGEN_FLAGS
helpviewer_keywords: COR_PRF_CODEGEN_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 3e184022-0247-4824-a23d-6b29593d8d01
topic_type: apiref
caps.latest.revision: "6"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c2c97510077fefd730827ac00326d267fd1c62ef
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="corprfcodegenflags-enumeration"></a><span data-ttu-id="aa14f-102">COR_PRF_CODEGEN_FLAGS (Enumeración)</span><span class="sxs-lookup"><span data-stu-id="aa14f-102">COR_PRF_CODEGEN_FLAGS Enumeration</span></span>
<span data-ttu-id="aa14f-103">Define las marcas de generación de código que se pueden establecer con el [icorprofilerfunctioncontrol:: Setcodegenflags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="aa14f-103">Defines the code generation flags that can be set with the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa14f-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa14f-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_CODEGEN_DISABLE_INLINING =          0x0001,  
    COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS = 0x0002,  
} COR_PRF_CODEGEN_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="aa14f-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa14f-105">Members</span></span>  
  
|<span data-ttu-id="aa14f-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="aa14f-106">Member</span></span>|<span data-ttu-id="aa14f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa14f-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_CODEGEN_DISABLE_INLINING`|<span data-ttu-id="aa14f-108">Ninguna función se insertarán entre línea en el cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="aa14f-108">No functions will be inlined into this function’s body.</span></span> <span data-ttu-id="aa14f-109">Sin embargo, la propia función puede insertarse en sus llamadores.</span><span class="sxs-lookup"><span data-stu-id="aa14f-109">However, the function itself may be inlined into its callers.</span></span>|  
|`COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS`|<span data-ttu-id="aa14f-110">Todas las optimizaciones se deshabilitará para el cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="aa14f-110">All optimizations will be disabled for this function’s body.</span></span> <span data-ttu-id="aa14f-111">Sin embargo, la propia función puede resultarle alinean en sus llamadores.</span><span class="sxs-lookup"><span data-stu-id="aa14f-111">However, the function itself may still be inlined into its callers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aa14f-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa14f-112">Remarks</span></span>  
 <span data-ttu-id="aa14f-113">El `COR_PRF_CODEGEN_FLAGS` enumeración es utilizada por la [icorprofilerfunctioncontrol:: Setcodegenflags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) método para habilitar el generador de perfiles controlar la generación de código para la función recompilada con JIT.</span><span class="sxs-lookup"><span data-stu-id="aa14f-113">The `COR_PRF_CODEGEN_FLAGS` enumeration is used by the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) method to enable the profiler to control the code generation for the JIT-recompiled function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa14f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa14f-114">Requirements</span></span>  
 <span data-ttu-id="aa14f-115">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aa14f-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa14f-116">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="aa14f-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="aa14f-117">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aa14f-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aa14f-118">**Versiones de .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aa14f-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa14f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa14f-119">See Also</span></span>  
 [<span data-ttu-id="aa14f-120">Enumeraciones de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="aa14f-120">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)