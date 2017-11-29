---
title: "EmitAssemblyCustomAttribute (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IALink.EmitAssemblyCustomAttribute
- EmitAssemblyCustomAttribute
api_location: alink.dll
api_type: COM
f1_keywords: EmitAssemblyCustomAttribute
helpviewer_keywords: EmitAssemblyCustomAttribute method
ms.assetid: b72f5409-79af-4fa7-90a7-7630eec170f1
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: bb21ee1396a9dd0426b9b91711c2345ef66c09f9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="emitassemblycustomattribute-method"></a><span data-ttu-id="a7282-102">EmitAssemblyCustomAttribute (Método)</span><span class="sxs-lookup"><span data-stu-id="a7282-102">EmitAssemblyCustomAttribute Method</span></span>
<span data-ttu-id="a7282-103">La llamada para establecer los atributos personalizados de nivel de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a7282-103">Call to set assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7282-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7282-104">Syntax</span></span>  
  
```  
HRESULT EmitAssemblyCustomAttribute(  
    mdAssembly   AssemblyID,  
    mdToken      FileToken,  
    mdToken      tkType,  
    void const*  pCustomValue,  
    DWORD        cbCustomValue,  
    BOOL         bSecurity,  
    BOOL         bAllowMulti  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a7282-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7282-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a7282-106">Identificador del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a7282-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="a7282-107">Archivo que define el atributo.</span><span class="sxs-lookup"><span data-stu-id="a7282-107">File that defiles the attribute.</span></span> <span data-ttu-id="a7282-108">Puede ser NULL si `AssemblyID` no indica un archivo netmodule no enlazado.</span><span class="sxs-lookup"><span data-stu-id="a7282-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `tkType`  
 <span data-ttu-id="a7282-109">Tipo del atributo personalizado.</span><span class="sxs-lookup"><span data-stu-id="a7282-109">Type of the custom attribute.</span></span>  
  
 `pCustomValue`  
 <span data-ttu-id="a7282-110">Datos del valor personalizado.</span><span class="sxs-lookup"><span data-stu-id="a7282-110">Custom value data.</span></span>  
  
 `cbCustomValue`  
 <span data-ttu-id="a7282-111">Longitud de datos del valor personalizado.</span><span class="sxs-lookup"><span data-stu-id="a7282-111">Length of custom value data.</span></span>  
  
 `bSecurity`  
 <span data-ttu-id="a7282-112">Es TRUE si el atributo personalizado está relacionado con la firma de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a7282-112">TRUE if the custom attribute is related to assembly signing.</span></span>  
  
 `bAllowMulti`  
 <span data-ttu-id="a7282-113">Es TRUE si hay varios atributos que se emitan.</span><span class="sxs-lookup"><span data-stu-id="a7282-113">TRUE if multiple attributes are to be emitted.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a7282-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7282-114">Return Value</span></span>  
 <span data-ttu-id="a7282-115">Devuelve S_OK si el método tiene éxito.</span><span class="sxs-lookup"><span data-stu-id="a7282-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7282-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7282-116">Requirements</span></span>  
 <span data-ttu-id="a7282-117">Requiere alink.h</span><span class="sxs-lookup"><span data-stu-id="a7282-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7282-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7282-118">See Also</span></span>  
 [<span data-ttu-id="a7282-119">IALink (interfaz)</span><span class="sxs-lookup"><span data-stu-id="a7282-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="a7282-120">IALink2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="a7282-120">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="a7282-121">API de ALink</span><span class="sxs-lookup"><span data-stu-id="a7282-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)