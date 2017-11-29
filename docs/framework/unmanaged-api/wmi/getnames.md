---
title: "GetNames (función) (referencia de API no administrada)"
description: "La función de GetNames recupera los nombres de las propiedades de un objeto."
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: GetNames
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: GetNames
helpviewer_keywords: GetNames function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2ba2530dd43e6924187c80214d5efa13ebc548de
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/15/2017
---
# <a name="getnames-function"></a><span data-ttu-id="4a680-103">GetNames (función)</span><span class="sxs-lookup"><span data-stu-id="4a680-103">GetNames function</span></span>
<span data-ttu-id="4a680-104">Recupera un subconjunto o todos los nombres de las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="4a680-104">Retrieves either a subset or all of the names of the properties of an object.</span></span> 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="4a680-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a680-105">Syntax</span></span>  
  
```  
HRESULT GetNames (
   [in] int                 vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LPCWSTR             wszQualifierName,
   [in] LONG                lFlags,
   [in] VARIANT*            pQualifierValue,
   [out] SAFEARRAY (BSTR)** pstrNames
); 
```  

## <a name="parameters"></a><span data-ttu-id="4a680-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a680-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="4a680-107">[in] Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4a680-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="4a680-108">[in] Un puntero a un [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instancia.</span><span class="sxs-lookup"><span data-stu-id="4a680-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>

`wszQualifierName`  
<span data-ttu-id="4a680-109">[in] Un puntero a un válido `LPCWSTR` que especifica un nombre de calificador que funciona como parte de un filtro.</span><span class="sxs-lookup"><span data-stu-id="4a680-109">[in] A pointer to a valid `LPCWSTR` that specifies a qualifier name that operates as part of a filter.</span></span> <span data-ttu-id="4a680-110">Para obtener más información, consulte el [comentarios](#remarks) sección.</span><span class="sxs-lookup"><span data-stu-id="4a680-110">For more information, see the [Remarks](#remarks) section.</span></span> <span data-ttu-id="4a680-111">Este parámetro puede ser `null`.</span><span class="sxs-lookup"><span data-stu-id="4a680-111">This parameter can be `null`.</span></span> 

`lFlags`  
<span data-ttu-id="4a680-112">[in] Una combinación de los campos de bits.</span><span class="sxs-lookup"><span data-stu-id="4a680-112">[in] A combination of bit fields.</span></span> <span data-ttu-id="4a680-113">Para obtener más información, consulte el [comentarios](#remarks) sección.</span><span class="sxs-lookup"><span data-stu-id="4a680-113">For more information, see the [Remarks](#remarks) section.</span></span>

`pQualifierValue`   
<span data-ttu-id="4a680-114">[in] Un puntero a un válido `VARIANT` estructura inicializada con un valor de filtro.</span><span class="sxs-lookup"><span data-stu-id="4a680-114">[in] A pointer to a valid `VARIANT` structure initialized to a filter value.</span></span> <span data-ttu-id="4a680-115">Este parámetro puede ser `null`.</span><span class="sxs-lookup"><span data-stu-id="4a680-115">This parameter can be `null`.</span></span> 

`pstrNames`  
<span data-ttu-id="4a680-116">[out] Un `SAFEARRAY` estructura que contiene los nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4a680-116">[out] A `SAFEARRAY` structure that contains property names.</span></span> <span data-ttu-id="4a680-117">En la entrada, este parámetro siempre debe ser un puntero a `null`.</span><span class="sxs-lookup"><span data-stu-id="4a680-117">On entry, this parameter must always be a pointer to `null`.</span></span> <span data-ttu-id="4a680-118">Consulte la [comentarios](#remarks) sección para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4a680-118">See the [Remarks](#remarks) section for more information.</span></span> 

## <a name="return-value"></a><span data-ttu-id="4a680-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a680-119">Return value</span></span>

<span data-ttu-id="4a680-120">Los siguientes valores devueltos por esta función se definen en el *WbemCli.h* archivo de encabezado, o bien puede definirlas como constantes en el código:</span><span class="sxs-lookup"><span data-stu-id="4a680-120">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="4a680-121">Constante</span><span class="sxs-lookup"><span data-stu-id="4a680-121">Constant</span></span>  |<span data-ttu-id="4a680-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4a680-122">Value</span></span>  |<span data-ttu-id="4a680-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a680-123">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="4a680-124">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="4a680-124">0x80041001</span></span> | <span data-ttu-id="4a680-125">Ha habido un error general.</span><span class="sxs-lookup"><span data-stu-id="4a680-125">There has been a general failure.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="4a680-126">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="4a680-126">0x80041008</span></span> | <span data-ttu-id="4a680-127">Uno o más parámetros no son válidos o se especificó una combinación incorrecta de marcas y los parámetros.</span><span class="sxs-lookup"><span data-stu-id="4a680-127">One or more parameters are not valid, or an incorrect combination of flags and parameters was specified.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="4a680-128">0 x 80041006</span><span class="sxs-lookup"><span data-stu-id="4a680-128">0x80041006</span></span> | <span data-ttu-id="4a680-129">No hay suficiente memoria disponible para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="4a680-129">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="4a680-130">0</span><span class="sxs-lookup"><span data-stu-id="4a680-130">0</span></span> | <span data-ttu-id="4a680-131">La llamada de función tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="4a680-131">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="4a680-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a680-132">Remarks</span></span>

<span data-ttu-id="4a680-133">Esta función contiene una llamada a la [IWbemClassObject::GetNames](https://msdn.microsoft.com/library/aa391447(v=vs.85).aspx) método.</span><span class="sxs-lookup"><span data-stu-id="4a680-133">This function wraps a call to the [IWbemClassObject::GetNames](https://msdn.microsoft.com/library/aa391447(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="4a680-134">El nombre devuelto se controla mediante una combinación de marcas y los parámetros.</span><span class="sxs-lookup"><span data-stu-id="4a680-134">The named returned are controlled by a combination of flags and parameters.</span></span> <span data-ttu-id="4a680-135">Por ejemplo, la función puede devolver los nombres de todas las propiedades o solo los nombres de las propiedades de clave.</span><span class="sxs-lookup"><span data-stu-id="4a680-135">For example, the function can return the names of all properties or only the names of the key properties.</span></span>  <span data-ttu-id="4a680-136">El filtro primario se especifica en el `lFlags` parámetro y los demás parámetros varían dependen de él.</span><span class="sxs-lookup"><span data-stu-id="4a680-136">The primary filter is specified in the `lFlags` parameter, and the other parameters vary depending on it.</span></span>

<span data-ttu-id="4a680-137">Valores de la marca de `lFlags` son campos de bits</span><span class="sxs-lookup"><span data-stu-id="4a680-137">The flag values in `lFlags` are bit fields</span></span>


<span data-ttu-id="4a680-138">Las marcas que se pueden pasar como el `lEnumFlags` argumento son campos de bits que se definen en el *WbemCli.h* archivo de encabezado, o bien puede definirlas como constantes en el código.</span><span class="sxs-lookup"><span data-stu-id="4a680-138">The flags that can be passed as the `lEnumFlags` argument are bit fields that are defined in the *WbemCli.h* header file, or you can define them as constants in your code.</span></span>  <span data-ttu-id="4a680-139">Puede combinar una marca de todos los grupos con cualquier marca de ningún otro grupo.</span><span class="sxs-lookup"><span data-stu-id="4a680-139">You can combine one flag from each group with any flag from any other group.</span></span> <span data-ttu-id="4a680-140">Sin embargo, las marcas del mismo grupo son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="4a680-140">However, flags from the same group are mutually exclusive.</span></span> 

| <span data-ttu-id="4a680-141">Indicadores de grupo 1</span><span class="sxs-lookup"><span data-stu-id="4a680-141">Group 1 flags</span></span> |<span data-ttu-id="4a680-142">Valor</span><span class="sxs-lookup"><span data-stu-id="4a680-142">Value</span></span>  |<span data-ttu-id="4a680-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a680-143">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAG_ALWAYS` | <span data-ttu-id="4a680-144">0</span><span class="sxs-lookup"><span data-stu-id="4a680-144">0</span></span> | <span data-ttu-id="4a680-145">Devolver todos los nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4a680-145">Return all property names.</span></span> <span data-ttu-id="4a680-146">`strQualifierName`y `pQualifierVal` están sin utilizar.</span><span class="sxs-lookup"><span data-stu-id="4a680-146">`strQualifierName` and `pQualifierVal` are unused.</span></span> |
| `WBEM_FLAG_ONLY_IF_TRUE` | <span data-ttu-id="4a680-147">1</span><span class="sxs-lookup"><span data-stu-id="4a680-147">1</span></span> | <span data-ttu-id="4a680-148">Devolver solo las propiedades que tienen un calificador del nombre especificado por el `strQualifierName` parámetro.</span><span class="sxs-lookup"><span data-stu-id="4a680-148">Return only properties that have a qualifier of the name specified by the `strQualifierName` parameter.</span></span> <span data-ttu-id="4a680-149">Si se usa esta marca, debe especificar `strQualifierName`.</span><span class="sxs-lookup"><span data-stu-id="4a680-149">If this flag is used, you must specify `strQualifierName`.</span></span> |
|`WBEM_FLAG_ONLY_IF_FALSE` | <span data-ttu-id="4a680-150">2</span><span class="sxs-lookup"><span data-stu-id="4a680-150">2</span></span> |  <span data-ttu-id="4a680-151">Devolver solo las propiedades que no tienen un calificador del nombre especificado por el `strQualifierName` parámetro.</span><span class="sxs-lookup"><span data-stu-id="4a680-151">Return only properties that do not have a qualifier of the name specified by the `strQualifierName` parameter.</span></span> <span data-ttu-id="4a680-152">Si se usa esta marca, debe especificar `strQualifierName`.</span><span class="sxs-lookup"><span data-stu-id="4a680-152">If this flag is used, you must specify `strQualifierName`.</span></span> |
|`WBEM_FLAG_ONLY_IF_IDENTICAL` | <span data-ttu-id="4a680-153">3</span><span class="sxs-lookup"><span data-stu-id="4a680-153">3</span></span> | <span data-ttu-id="4a680-154">Devolver solo las propiedades que tienen un calificador del nombre especificado por el `wszQualifierName` parámetro y también tienen un valor idéntico al especificado por el `pQualifierVal` estructura.</span><span class="sxs-lookup"><span data-stu-id="4a680-154">Return only properties that have a qualifier of the name specified by the `wszQualifierName` parameter and also have a value identical to that specified by the `pQualifierVal` structure.</span></span> <span data-ttu-id="4a680-155">Si se utiliza esta marca, debe especificar tanto una `wszQualifierName` y `pQualifierValue`.</span><span class="sxs-lookup"><span data-stu-id="4a680-155">If this flag is used, you must specify both a `wszQualifierName` and a `pQualifierValue`.</span></span> |

| <span data-ttu-id="4a680-156">Indicadores de grupo 2</span><span class="sxs-lookup"><span data-stu-id="4a680-156">Group 2 flags</span></span> |<span data-ttu-id="4a680-157">Valor</span><span class="sxs-lookup"><span data-stu-id="4a680-157">Value</span></span>  |<span data-ttu-id="4a680-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a680-158">Description</span></span>  |
|---------|---------|---------|
|`WBEM_FLAG_KEYS_ONLY` | <span data-ttu-id="4a680-159">0 x 4</span><span class="sxs-lookup"><span data-stu-id="4a680-159">0x4</span></span> | <span data-ttu-id="4a680-160">Devolver solo los nombres de propiedades que definen las claves.</span><span class="sxs-lookup"><span data-stu-id="4a680-160">Return only the names of properties that define the keys.</span></span> |
|`WBEM_FLAG_REFS_ONLY` | <span data-ttu-id="4a680-161">0 x 8</span><span class="sxs-lookup"><span data-stu-id="4a680-161">0x8</span></span> | <span data-ttu-id="4a680-162">Valor devuelto solo nombres de propiedad que son referencias de objeto.</span><span class="sxs-lookup"><span data-stu-id="4a680-162">Return only property names that are object references.</span></span> |

| <span data-ttu-id="4a680-163">Indicadores de grupo 3</span><span class="sxs-lookup"><span data-stu-id="4a680-163">Group 3 flags</span></span> |<span data-ttu-id="4a680-164">Valor</span><span class="sxs-lookup"><span data-stu-id="4a680-164">Value</span></span>  |<span data-ttu-id="4a680-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a680-165">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAG_LOCAL_ONLY` | <span data-ttu-id="4a680-166">0 x 10</span><span class="sxs-lookup"><span data-stu-id="4a680-166">0x10</span></span> | <span data-ttu-id="4a680-167">Devolver solo los nombres de propiedad que pertenecen a la clase más derivada.</span><span class="sxs-lookup"><span data-stu-id="4a680-167">Return only property names that belong to the most derived class.</span></span> <span data-ttu-id="4a680-168">Excluir propiedades de las clases principales.</span><span class="sxs-lookup"><span data-stu-id="4a680-168">Exclude properties from the parent classes.</span></span> |
| `WBEM_FLAG_PROPAGATED_ONLY` |  <span data-ttu-id="4a680-169">0 x 20</span><span class="sxs-lookup"><span data-stu-id="4a680-169">0x20</span></span> | <span data-ttu-id="4a680-170">Devolver solo los nombres de propiedad que pertenecen a las clases principales.</span><span class="sxs-lookup"><span data-stu-id="4a680-170">Return only property names that belong to the parent classes.</span></span> |
|`WBEM_FLAG_SYSTEM_ONLY` | <span data-ttu-id="4a680-171">0 x 30</span><span class="sxs-lookup"><span data-stu-id="4a680-171">0x30</span></span> | <span data-ttu-id="4a680-172">Devolver solo los nombres de propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a680-172">Return only the names of system properties.</span></span> |
|`WBEM_FLAG_NONSYSTEM_ONLY` | <span data-ttu-id="4a680-173">0 x 40</span><span class="sxs-lookup"><span data-stu-id="4a680-173">0x40</span></span> | <span data-ttu-id="4a680-174">Devolver solo los nombres de propiedades no son del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a680-174">Return only the names of non-system properties.</span></span> |

<span data-ttu-id="4a680-175">La función siempre asigna un nuevo `SAFEARRAY` si devuelve `WBEM_S_NO_ERROR`, y `pstrNames` siempre se establece para que apunte a él.</span><span class="sxs-lookup"><span data-stu-id="4a680-175">The function always allocates a new `SAFEARRAY` if it returns `WBEM_S_NO_ERROR`, and `pstrNames` is always set to point to it.</span></span> <span data-ttu-id="4a680-176">La matriz devuelta puede tener 0 elementos si no hay propiedades coinciden con los filtros especificados.</span><span class="sxs-lookup"><span data-stu-id="4a680-176">The returned array can have 0 elements if no properties match the specified filters.</span></span> <span data-ttu-id="4a680-177">Si la función devuelve un valor distinto de `WBM_S_NO_ERROR`, un nuevo `SAFEARRAY` estructura no se devuelve.</span><span class="sxs-lookup"><span data-stu-id="4a680-177">If the function returns an value other than `WBM_S_NO_ERROR`, a new `SAFEARRAY` structure is not returned.</span></span>
 
## <a name="requirements"></a><span data-ttu-id="4a680-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a680-178">Requirements</span></span>  
 <span data-ttu-id="4a680-179">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4a680-179">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a680-180">**Encabezado:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="4a680-180">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="4a680-181">**Versiones de .NET framework:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4a680-181">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a680-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a680-182">See also</span></span>  
[<span data-ttu-id="4a680-183">WMI y contadores de rendimiento (referencia de API no administrada)</span><span class="sxs-lookup"><span data-stu-id="4a680-183">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)