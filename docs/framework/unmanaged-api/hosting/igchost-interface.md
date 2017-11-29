---
title: IGCHost (Interfaz)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IGCHost
api_location: mscoree.dll
api_type: COM
f1_keywords: IGCHost
helpviewer_keywords: IGCHost interface [.NET Framework hosting]
ms.assetid: 9ad70ffd-6963-4ab2-8c84-3d86c3fb8deb
topic_type: apiref
caps.latest.revision: "15"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5c0f398c09569a855291a1565ce63b513161a803
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="igchost-interface"></a><span data-ttu-id="185ca-102">IGCHost (Interfaz)</span><span class="sxs-lookup"><span data-stu-id="185ca-102">IGCHost Interface</span></span>
<span data-ttu-id="185ca-103">Proporciona métodos para obtener información sobre el sistema de recopilación de elementos no utilizados y para controlar algunos aspectos de la recolección de elementos.</span><span class="sxs-lookup"><span data-stu-id="185ca-103">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="185ca-104">A partir de la [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], puede usar el [igchost2:: Setgcstartuplimitsex](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) método para establecer el tamaño de un segmento de la colección de elementos no utilizados y el tamaño máximo de la generación 0 del sistema de recopilación de elementos no utilizados en valores mayor que el `DWORD` límite impuesto por la [SetGCStartupLimits](../../../../docs/framework/unmanaged-api/hosting/igchost-setgcstartuplimits-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="185ca-104">Starting with the [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], you can use the [IGCHost2::SetGCStartupLimitsEx](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) method to set the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0 to values greater than the `DWORD` limit that is imposed by the [SetGCStartupLimits](../../../../docs/framework/unmanaged-api/hosting/igchost-setgcstartuplimits-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="185ca-105">Esta interfaz es solo pueden utilizar expertos.</span><span class="sxs-lookup"><span data-stu-id="185ca-105">This interface is for expert usage only.</span></span> <span data-ttu-id="185ca-106">Si se utiliza incorrectamente puede afectar al rendimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="185ca-106">It can affect the performance of an application if used improperly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="185ca-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="185ca-107">Methods</span></span>  
  
|<span data-ttu-id="185ca-108">Método</span><span class="sxs-lookup"><span data-stu-id="185ca-108">Method</span></span>|<span data-ttu-id="185ca-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="185ca-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="185ca-110">Collect (método)</span><span class="sxs-lookup"><span data-stu-id="185ca-110">Collect Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-collect-method.md)|<span data-ttu-id="185ca-111">Fuerza una recolección que se produzca la generación determinada, con independencia del estado de la colección de elementos no utilizados actual.</span><span class="sxs-lookup"><span data-stu-id="185ca-111">Forces a collection to occur for the given generation, regardless of the state of the current garbage collection.</span></span>|  
|[<span data-ttu-id="185ca-112">GetStats (método)</span><span class="sxs-lookup"><span data-stu-id="185ca-112">GetStats Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-getstats-method.md)|<span data-ttu-id="185ca-113">Obtiene las estadísticas para el estado actual del sistema de recopilación de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="185ca-113">Gets the statistics for the current state of the garbage collection system.</span></span>|  
|[<span data-ttu-id="185ca-114">GetThreadStats (método)</span><span class="sxs-lookup"><span data-stu-id="185ca-114">GetThreadStats Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-getthreadstats-method.md)|<span data-ttu-id="185ca-115">Obtiene las estadísticas por subproceso para la recolección.</span><span class="sxs-lookup"><span data-stu-id="185ca-115">Gets the per-thread statistics for garbage collection.</span></span>|  
|[<span data-ttu-id="185ca-116">SetGCStartupLimits (método)</span><span class="sxs-lookup"><span data-stu-id="185ca-116">SetGCStartupLimits Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-setgcstartuplimits-method.md)|<span data-ttu-id="185ca-117">Establece el tamaño del segmento y el tamaño máximo para la generación 0.</span><span class="sxs-lookup"><span data-stu-id="185ca-117">Sets the segment size and the maximum size for generation 0.</span></span>|  
|[<span data-ttu-id="185ca-118">SetVirtualMemLimit (método)</span><span class="sxs-lookup"><span data-stu-id="185ca-118">SetVirtualMemLimit Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-setvirtualmemlimit-method.md)|<span data-ttu-id="185ca-119">Establece el tamaño máximo de memoria virtual de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="185ca-119">Sets the maximum size of the runtime's virtual memory.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="185ca-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="185ca-120">Requirements</span></span>  
 <span data-ttu-id="185ca-121">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="185ca-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="185ca-122">**Encabezado:** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="185ca-122">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="185ca-123">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="185ca-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="185ca-124">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="185ca-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="185ca-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="185ca-125">See Also</span></span>  
 [<span data-ttu-id="185ca-126">Interfaces de hospedaje</span><span class="sxs-lookup"><span data-stu-id="185ca-126">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="185ca-127">CorRuntimeHost (Coclase)</span><span class="sxs-lookup"><span data-stu-id="185ca-127">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)