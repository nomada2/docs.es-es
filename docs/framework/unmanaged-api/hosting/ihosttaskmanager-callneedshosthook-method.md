---
title: "IHostTaskManager::CallNeedsHostHook (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostTaskManager.CallNeedsHostHook
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostTaskManager::CallNeedsHostHook
helpviewer_keywords:
- CallNeedsHostHook method [.NET Framework hosting]
- IHostTaskManager::CallNeedsHostHook method [.NET Framework hosting]
ms.assetid: b60f1f59-9825-4b57-961f-d2979518e6a7
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0daa122b3576c1a6e6e192a4992549e704721bb4
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="ihosttaskmanagercallneedshosthook-method"></a><span data-ttu-id="2b401-102">IHostTaskManager::CallNeedsHostHook (Método)</span><span class="sxs-lookup"><span data-stu-id="2b401-102">IHostTaskManager::CallNeedsHostHook Method</span></span>
<span data-ttu-id="2b401-103">Permite al host especificar si common language runtime (CLR) puede procesar en línea la llamada especificada a una función no administrada.</span><span class="sxs-lookup"><span data-stu-id="2b401-103">Enables the host to specify whether the common language runtime (CLR) can inline the specified call to an unmanaged function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b401-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b401-104">Syntax</span></span>  
  
```  
HRESULT CallNeedsHostHook (  
    [in]  SIZE_T target,   
    [out] BOOL   *pbCallNeedsHostHook  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2b401-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b401-105">Parameters</span></span>  
 `target`  
 <span data-ttu-id="2b401-106">[in] La dirección en el archivo asignado archivo portable ejecutable (PE) de la función no administrada que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="2b401-106">[in] The address within the mapped portable executable (PE) file of the unmanaged function that is to be called.</span></span>  
  
 `pbCallNeedsHostHook`  
 <span data-ttu-id="2b401-107">[out] Un puntero a un valor booleano que indica si el host requiere que se puede enlazar la llamada.</span><span class="sxs-lookup"><span data-stu-id="2b401-107">[out] A pointer to a Boolean value that indicates whether the host requires the call to be hooked.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2b401-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b401-108">Return Value</span></span>  
  
|<span data-ttu-id="2b401-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2b401-109">HRESULT</span></span>|<span data-ttu-id="2b401-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b401-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2b401-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b401-111">S_OK</span></span>|<span data-ttu-id="2b401-112">`CallNeedsHostHook`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b401-112">`CallNeedsHostHook` returned successfully.</span></span>|  
|<span data-ttu-id="2b401-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2b401-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2b401-114">El CLR no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b401-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2b401-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2b401-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2b401-116">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="2b401-116">The call timed out.</span></span>|  
|<span data-ttu-id="2b401-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2b401-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2b401-118">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="2b401-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2b401-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2b401-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2b401-120">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="2b401-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2b401-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2b401-121">E_FAIL</span></span>|<span data-ttu-id="2b401-122">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="2b401-122">An unknown catastrophic failure has occurred.</span></span> <span data-ttu-id="2b401-123">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="2b401-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2b401-124">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="2b401-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2b401-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b401-125">Remarks</span></span>  
 <span data-ttu-id="2b401-126">Con el fin de optimizar la ejecución de código, el CLR realiza un análisis de cada plataforma de llamada de invocación de durante la compilación para determinar si se puede alinear la llamada.</span><span class="sxs-lookup"><span data-stu-id="2b401-126">To help optimize code execution, the CLR performs an analysis of each platform invoke call during compilation to determine whether the call can be inlined.</span></span> <span data-ttu-id="2b401-127">`CallNeedsHostHook`permite al host reemplazar esa decisión exigiendo que se puede enlazar una llamada a una función no administrada.</span><span class="sxs-lookup"><span data-stu-id="2b401-127">`CallNeedsHostHook` enables the host to override that decision by requiring that a call to an unmanaged function be hooked.</span></span> <span data-ttu-id="2b401-128">Si el host requiere un enlace, el tiempo de ejecución no alinea la llamada.</span><span class="sxs-lookup"><span data-stu-id="2b401-128">If the host requires a hook, the runtime does not inline the call.</span></span>  
  
 <span data-ttu-id="2b401-129">El host normalmente requeriría un enlace donde debe ajustar un estado de punto flotante, o tras recibir la notificación de que una llamada está entrando en un estado donde el host no puede realizar un seguimiento de las solicitudes de tiempo de ejecución para memoria o cualquier bloqueo tomado.</span><span class="sxs-lookup"><span data-stu-id="2b401-129">The host typically would require a hook where it must adjust a floating-point state, or upon receiving notification that a call is entering a state where the host cannot track the runtime's requests for memory or any locks taken.</span></span> <span data-ttu-id="2b401-130">Cuando el host requiere que se enlace la llamada, el tiempo de ejecución notifica al host de las transiciones a y desde el código administrado mediante llamadas a [EnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enterruntime-method.md), [LeaveRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-leaveruntime-method.md), [ ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md), y [ReverseLeaveRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseleaveruntime-method.md).</span><span class="sxs-lookup"><span data-stu-id="2b401-130">When the host requires that the call be hooked, the runtime notifies the host of transitions to and from managed code by using calls to [EnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enterruntime-method.md), [LeaveRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-leaveruntime-method.md), [ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md), and [ReverseLeaveRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseleaveruntime-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b401-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b401-131">Requirements</span></span>  
 <span data-ttu-id="2b401-132">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b401-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b401-133">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2b401-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2b401-134">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2b401-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2b401-135">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b401-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b401-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b401-136">See Also</span></span>  
 [<span data-ttu-id="2b401-137">ICLRTask (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2b401-137">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="2b401-138">ICLRTaskManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2b401-138">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="2b401-139">IHostTask (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2b401-139">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="2b401-140">IHostTaskManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2b401-140">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)