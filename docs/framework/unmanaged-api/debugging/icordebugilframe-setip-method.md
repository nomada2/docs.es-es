---
title: ICorDebugILFrame::SetIP (Método)
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.SetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::SetIP
helpviewer_keywords:
- SetIP method, ICorDebugILFrame interface [.NET Framework debugging]
- ICorDebugILFrame::SetIP method [.NET Framework debugging]
ms.assetid: 23f38dc1-85e4-4263-9235-2d05bbb6a833
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ed7de70c8ea26f46f44abb3e063c6e4c4b115666
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414495"
---
# <a name="icordebugilframesetip-method"></a>ICorDebugILFrame::SetIP (Método)
Establece el puntero de instrucción en la ubicación de desplazamiento especificada en el código de lenguaje intermedio (MSIL) de Microsoft.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
HRESULT SetIP (  
    [in] ULONG32 nOffset  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `nOffset`  
 La ubicación de desplazamiento en el código MSIL.  
  
## <a name="remarks"></a>Comentarios  
 Las llamadas a `SetIP` inmediatamente invalidar todos los marcos y cadenas para el subproceso actual. Si el depurador necesita información del marco después de llamar a `SetIP`, debe realizar un seguimiento de pila nueva.  
  
 [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) intentará mantener el marco de pila en un estado válido. Sin embargo, incluso si el marco está en un estado válido, todavía puede haber problemas, como variables locales sin inicializar. El llamador es responsable de garantizar la coherencia del programa en ejecución.  
  
 En plataformas de 64 bits, no se puede mover el puntero de instrucción fuera de un `catch` o `finally` bloque. Si `SetIP` se llama para hacer ese cambio en una plataforma de 64 bits, devolverá un valor HRESULT que indica un error.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado:** CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **Versiones de .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
