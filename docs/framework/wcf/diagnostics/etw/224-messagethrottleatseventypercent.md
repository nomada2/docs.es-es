---
title: 224 - MessageThrottleAtSeventyPercent
ms.date: 03/30/2017
ms.assetid: 82bbbfd7-10d2-41fd-805d-2443b0c1b96b
ms.openlocfilehash: f70dc235e037b4f490a25866940fe2bccceae2a1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
---
# <a name="224---messagethrottleatseventypercent"></a>224 - MessageThrottleAtSeventyPercent
## <a name="properties"></a>Propiedades  
  
|||  
|-|-|  
|Id.|224|  
|Palabras clave|EndToEndMonitoring, HealthMonitoring, Solución de problemas, ServiceModel|  
|Nivel|Advertencia|  
|Canal|Microsoft-Windows-Application Server-Applications/Analytic|  
  
## <a name="description"></a>Descripción  
 Cuando se ha superado uno de los aceleradores del servicio principal, se emite el evento `MessageThrottleExceeded`. Cuando la punta de actividad se retrasa y el valor actual del acelerador está al 70 por ciento del límite actual, entonces se emite este evento. Tenga en cuenta que este evento solo se emite una vez cuando la actividad se retrasa. Si el valor actual oscila alrededor del valor del 70 por ciento (por ejemplo, 70, 69, 70, 71, 70, 69), solo la primera aparición del 70 por ciento producirá un evento. Una vez emitido este evento, las situaciones futuras de superación del límite del acelerador resultarán en un evento `MessageThrottleExceeded`.  
  
## <a name="message"></a>Mensaje  
 La limitación '%1' de '%2' se encuentra al 70%.  
  
## <a name="details"></a>Detalles  
  
|Nombre del elemento de datos|Tipo del elemento de datos|Descripción|  
|--------------------|--------------------|-----------------|  
|Throttle Name|`xs:string`|El nombre del acelerador que se ha superado. `MaxConcurrentCalls`, `MaxConcurrentInstances` o `MaxConcurrentSessions`,|  
|Limit|`xs:long`|El límite configurado actual del acelerador.|  
|HostReference|`xs:string`|En el caso de los servicios hospedados en web, este campo identifica de manera única el servicio en la jerarquía web. El formato se define como ' ruta de acceso Virtual de sitio Web de nombre aplicación&#124;ruta de acceso Virtual del servicio&#124;ServiceName'. Ejemplo: ' predeterminado sitio Web/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.|  
|AppDomain|`xs:string`|La cadena devuelta por AppDomain.CurrentDomain.FriendlyName.|
