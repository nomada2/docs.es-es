---
title: Objetos y características de subprocesos
ms.date: 10/01/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 745cd1e17e2c06a513c6fdafe8f6b5f464b95d5f
ms.sourcegitcommit: dcc8feeff4718664087747529638ec9b47e65234
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/31/2019
ms.locfileid: "55479664"
---
# <a name="threading-objects-and-features"></a>Objetos y características de subprocesos

Junto con la clase <xref:System.Threading.Thread?displayProperty=nameWithType>, .NET proporciona una serie de clases que le ayudarán a desarrollar aplicaciones multiproceso. En los siguientes artículos encontrará información general sobre estas clases:

|Title|Descripción|  
|-----------|-----------------|  
|[Grupo de subprocesos administrado](the-managed-thread-pool.md)|Describe cómo usar la clase <xref:System.Threading.ThreadPool?displayProperty=nameWithType>, que proporciona un grupo de subprocesos de trabajo administrados por .NET.|  
|[Timers](timers.md) (Temporizadores)|Describe los temporizadores de .NET que se pueden usar en un entorno multiproceso.|
|[Información general sobre las primitivas de sincronización](overview-of-synchronization-primitives.md)|Describe los tipos que se pueden usar para sincronizar el acceso a un recurso compartido o la interacción del subproceso de control.|
|[EventWaitHandle, CountdownEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|Describe los identificadores de espera de eventos administrados, que se usan para sincronizar las actividades del subproceso mediante señalización y señales de espera.|
|[Mutexes](mutexes.md) (Clases Mutex)|Describe <xref:System.Threading.Mutex?displayProperty=nameWithType>, que concede acceso exclusivo a un recurso compartido.|
|[Semaphore and SemaphoreSlim](semaphore-and-semaphoreslim.md) (Clases Semaphore y SemaphoreSlim)|Describe la clase <xref:System.Threading.Semaphore?displayProperty=nameWithType>, que limita el número de subprocesos que pueden tener acceso a un recurso compartido o grupo de recursos simultáneamente.|
|[Barrier](barrier.md) (Barrera)|Describe la clase <xref:System.Threading.Barrier?displayProperty=nameWithType> que implementa el modelo de barrera para coordinar los subprocesos en las operaciones por fases.|
|[SpinLock](spinlock.md)|Describe la estructura <xref:System.Threading.SpinLock?displayProperty=nameWithType>, que es una alternativa ligera a la clase <xref:System.Threading.Monitor?displayProperty=nameWithType> para algunos escenarios de bloqueo de bajo nivel.|
|[SpinWait](spinwait.md)|Describe la estructura <xref:System.Threading.SpinWait?displayProperty=nameWithType>, que proporciona compatibilidad para la espera basada en ciclos.|

## <a name="see-also"></a>Vea también

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [Uso de subprocesos y subprocesamiento](using-threads-and-threading.md)
- [Asynchronous File I/O](../io/asynchronous-file-i-o.md)
- [Programación en paralelo](../parallel-programming/index.md)
- [Biblioteca TPL](../parallel-programming/task-parallel-library-tpl.md)
