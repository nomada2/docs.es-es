---
title: "ICorProfilerCallback::ModuleUnloadStarted (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ModuleUnloadStarted
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ModuleUnloadStarted
helpviewer_keywords:
- ModuleUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ModuleUnloadStarted method [.NET Framework profiling]
ms.assetid: 2debcaab-6005-4245-afdb-4268bb7e74bd
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 069e47ad3d1dd9459b7344b1af1a2ad6d32305ab
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackmoduleunloadstarted-method"></a><span data-ttu-id="6ddea-102">ICorProfilerCallback::ModuleUnloadStarted (Método)</span><span class="sxs-lookup"><span data-stu-id="6ddea-102">ICorProfilerCallback::ModuleUnloadStarted Method</span></span>
<span data-ttu-id="6ddea-103">Notifica al generador de perfiles que un módulo se está descargando.</span><span class="sxs-lookup"><span data-stu-id="6ddea-103">Notifies the profiler that a module is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ddea-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ddea-104">Syntax</span></span>  
  
```  
HRESULT ModuleUnloadStarted(  
    [in] ModuleID moduleId);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="6ddea-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ddea-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="6ddea-106">[in] El identificador del módulo que se está descargando.</span><span class="sxs-lookup"><span data-stu-id="6ddea-106">[in] The ID of the module that is being unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6ddea-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ddea-107">Remarks</span></span>  
 <span data-ttu-id="6ddea-108">El valor de `moduleId` no es válido para una solicitud de información después de la `ModuleUnloadStarted` devuelve del método: se trata de la última oportunidad para obtener información acerca de este módulo del generador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="6ddea-108">The value of `moduleId` is not valid for an information request after the `ModuleUnloadStarted` method returns — this is the profiler's last chance to get information about this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ddea-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ddea-109">Requirements</span></span>  
 <span data-ttu-id="6ddea-110">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6ddea-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ddea-111">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6ddea-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6ddea-112">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6ddea-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6ddea-113">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ddea-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ddea-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ddea-114">See Also</span></span>  
 [<span data-ttu-id="6ddea-115">ICorProfilerCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="6ddea-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="6ddea-116">ModuleUnloadFinished (método)</span><span class="sxs-lookup"><span data-stu-id="6ddea-116">ModuleUnloadFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleunloadfinished-method.md)