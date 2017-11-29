---
title: "CorBindToCurrentRuntime (Función)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorBindToCurrentRuntime
api_location:
- mscoree.dll
- mscoreei.dll
api_type: HeaderDef
f1_keywords: CorBindToCurrentRuntime
helpviewer_keywords: CorBindToCurrentRuntime function [.NET Framework hosting]
ms.assetid: 6105c13e-d9cd-44d2-a95a-924e042830c7
topic_type: apiref
caps.latest.revision: "22"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 630dab4fec8c37bd776b68870a53ab20e4050e06
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="corbindtocurrentruntime-function"></a><span data-ttu-id="6a8c5-102">CorBindToCurrentRuntime (Función)</span><span class="sxs-lookup"><span data-stu-id="6a8c5-102">CorBindToCurrentRuntime Function</span></span>
<span data-ttu-id="6a8c5-103">Carga common language runtime (CLR) en un proceso usando la información de versión almacenada en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-103">Loads the common language runtime (CLR) into a process by using version information stored in an XML file.</span></span> <span data-ttu-id="6a8c5-104">El formato del archivo XML se modela después del archivo de configuración de aplicación estándar.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-104">The format of the XML file is modeled after the standard application configuration file.</span></span> <span data-ttu-id="6a8c5-105">Para más información sobre los archivos de configuración, vea [Configuration File Schema](../../../../docs/framework/configure-apps/file-schema/index.md) (Esquema de archivos de configuración).</span><span class="sxs-lookup"><span data-stu-id="6a8c5-105">For more information about configuration files, see [Configuration File Schema](../../../../docs/framework/configure-apps/file-schema/index.md).</span></span>  
  
 <span data-ttu-id="6a8c5-106">Esta función está desusada en [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a8c5-106">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="6a8c5-107">Vea [cargar Common Language Runtime en un proceso](http://msdn.microsoft.com/en-us/1e2d6dc1-6aab-43e2-bbc0-aae40756d24f).</span><span class="sxs-lookup"><span data-stu-id="6a8c5-107">See [Loading the Common Language Runtime into a Process](http://msdn.microsoft.com/en-us/1e2d6dc1-6aab-43e2-bbc0-aae40756d24f).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a8c5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a8c5-108">Syntax</span></span>  
  
```  
HRESULT CorBindToCurrentRuntime (  
    [in]  LPCWSTR   pwszFileName,  
    [in]  REFCLSID  rclsid,  
    [in]  REFIID    riid,  
    [out] LPVOID    *ppv  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6a8c5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a8c5-109">Parameters</span></span>  
 `pwszFileName`  
 <span data-ttu-id="6a8c5-110">[in] El nombre de un archivo de configuración que especifica la versión de CLR que se debe cargar.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-110">[in] The name of an application configuration file that specifies the version of the CLR to load.</span></span> <span data-ttu-id="6a8c5-111">Si el nombre de archivo no está completo, se supone que en el mismo directorio que el ejecutable que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-111">If the file name is not fully qualified, it is assumed to be in the same directory as the executable making the call.</span></span>  
  
 <span data-ttu-id="6a8c5-112">La versión de runtime que se va a cargar se describe mediante el atributo de versión en la [ \<requiredRuntime >](../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md) elemento del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-112">The version of the runtime to be loaded is described by the version attribute in the [\<requiredRuntime>](../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md) element of the configuration file.</span></span>  
  
 <span data-ttu-id="6a8c5-113">Si no se especifica ninguna versión, o si la `<requiredRuntime>` no se encuentra el elemento, se cargará la versión más reciente de CLR que está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-113">If no version is specified, or if the `<requiredRuntime>` element cannot be found, the latest version of the CLR that is installed on the machine is loaded.</span></span>  
  
 `rclsid`  
 <span data-ttu-id="6a8c5-114">[in] El `CLSID` de la coclase que implementa la [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) o [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-114">[in] The `CLSID` of the coclass that implements either the [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) or the [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interface.</span></span> <span data-ttu-id="6a8c5-115">Los valores admitidos son CLSID_CorRuntimeHost o CLSID_CLRRuntimeHost.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-115">Supported values are CLSID_CorRuntimeHost or CLSID_CLRRuntimeHost.</span></span>  
  
 `riid`  
 <span data-ttu-id="6a8c5-116">[in] El `IID` de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-116">[in] The `IID` of the interface you are requesting.</span></span> <span data-ttu-id="6a8c5-117">Los valores admitidos son IID_ICorRuntimeHost o IID_ICLRRuntimeHost.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-117">Supported values are IID_ICorRuntimeHost or IID_ICLRRuntimeHost.</span></span>  
  
 `ppv`  
 <span data-ttu-id="6a8c5-118">[out] El puntero de interfaz devuelto.</span><span class="sxs-lookup"><span data-stu-id="6a8c5-118">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a8c5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a8c5-119">Requirements</span></span>  
 <span data-ttu-id="6a8c5-120">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6a8c5-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a8c5-121">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6a8c5-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6a8c5-122">**Biblioteca:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6a8c5-122">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6a8c5-123">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a8c5-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a8c5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a8c5-124">See Also</span></span>  
 [<span data-ttu-id="6a8c5-125">CorBindToRuntime (función)</span><span class="sxs-lookup"><span data-stu-id="6a8c5-125">CorBindToRuntime Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md)  
 [<span data-ttu-id="6a8c5-126">CorBindToRuntimeByCfg (función)</span><span class="sxs-lookup"><span data-stu-id="6a8c5-126">CorBindToRuntimeByCfg Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)  
 [<span data-ttu-id="6a8c5-127">CorBindToRuntimeEx (función)</span><span class="sxs-lookup"><span data-stu-id="6a8c5-127">CorBindToRuntimeEx Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)  
 [<span data-ttu-id="6a8c5-128">CorBindToRuntimeHost (función)</span><span class="sxs-lookup"><span data-stu-id="6a8c5-128">CorBindToRuntimeHost Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md)  
 [<span data-ttu-id="6a8c5-129">ICorRuntimeHost (interfaz)</span><span class="sxs-lookup"><span data-stu-id="6a8c5-129">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)  
 [<span data-ttu-id="6a8c5-130">Funciones de hospedaje de CLR en desuso</span><span class="sxs-lookup"><span data-stu-id="6a8c5-130">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)