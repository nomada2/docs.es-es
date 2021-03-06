---
title: Procedimiento Generar manualmente clases de servicio de datos de cliente (WCF Data Services)
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, configuring
- WCF Data Services, client library
ms.assetid: b98cb1d6-956a-4e50-add6-67e4f2587346
ms.openlocfilehash: c95ad9371854257059861b7d1e48c7afbc957ea1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54613235"
---
# <a name="how-to-manually-generate-client-data-service-classes-wcf-data-services"></a>Procedimiento Generar manualmente clases de servicio de datos de cliente (WCF Data Services)
WCF Data Services se integra con Visual Studio que le permite generar automáticamente clases de servicio de datos de cliente cuando se usa el **Add Service Reference** cuadro de diálogo para agregar una referencia a un servicio de datos en un proyecto de Visual Studio. Para obtener más información, vea [Cómo: Agregar una referencia de servicio de datos](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md). También puede generar manualmente las mismas clases del servicio de datos del cliente mediante la herramienta de generación de código `DataSvcUtil.exe`. Esta herramienta, que se incluye con WCF Data Services, genera clases de .NET Framework de la definición de servicio de datos. También se puede usar para generar clases del servicio de datos a partir del archivo de modelo conceptual (.csdl) y del archivo .edmx que representa un modelo de Entity Framework en un proyecto Visual Studio.

 El ejemplo usado en este tema crea clases del servicio de datos del cliente basadas en el servicio de datos de ejemplo de Northwind. Este servicio se crea al completar el [inicio rápido de WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md). Algunos ejemplos de este tema requieren el archivo de modelo conceptual para el modelo de Northwind. Para obtener más información, vea [Cómo: Usar EdmGen.exe para generar los archivos de asignación y modelo](../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md). Algunos ejemplos de este tema requieren el archivo de modelo conceptual .edmx para el modelo de Northwind. Para obtener más información, consulte [información general del archivo .edmx](https://msdn.microsoft.com/library/f4c8e7ce-1db6-417e-9759-15f8b55155d4).

### <a name="to-generate-c-classes-that-support-data-binding"></a>Para generar clases de C# que admitan el enlace de datos

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```console
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /dataservicecollection /version:2.0 /language:CSharp /out:Northwind.cs /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Debe reemplazar el valor proporcionado para el parámetro `/uri:` con el URI de la instancia del servicio de datos de ejemplo de Northwind.

### <a name="to-generate-visual-basic-classes-that-support-data-binding"></a>Para generar clases Visual Basic que admitan el enlace de datos

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```console
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /dataservicecollection /version:2.0 /language:VB /out:Northwind.vb /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Debe reemplazar el valor proporcionado para el parámetro `/uri:` con el URI de la instancia del servicio de datos de ejemplo de Northwind.

### <a name="to-generate-c-classes-based-on-the-service-uri"></a>Para generar clases de C# basadas en el URI de servicio

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /language:CSharp /out:northwind.cs /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Debe reemplazar el valor proporcionado para el parámetro `/uri:` con el URI de la instancia del servicio de datos de ejemplo de Northwind.

### <a name="to-generate-visual-basic-classes-based-on-the-service-uri"></a>Para generar clases de Visual Basic basadas en el URI de servicio

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /out:Northwind.vb /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Debe reemplazar el valor proporcionado para el parámetro `/uri:` con el URI de la instancia del servicio de datos de ejemplo de Northwind.

### <a name="to-generate-c-classes-based-on-the-conceptual-model-file-csdl"></a>Para generar clases de C# basadas en el archivo de modelo conceptual (CSDL)

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:CSharp /in:Northwind.csdl /out:Northwind.cs
    ```

### <a name="to-generate-visual-basic-classes-based-on-the-conceptual-model-file-csdl"></a>Para generar clases de Visual Basic basadas en el archivo de modelo conceptual (CSDL)

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /in:Northwind.csdl /out:Northwind.vb
    ```

### <a name="to-generate-c-classes-based-on-the-edmx-file"></a>Para generar clases de C# basadas en el archivo .edmx

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:CSharp /in:Northwind.edmx /out:c:\northwind.cs
    ```

### <a name="to-generate-visual-basic-classes-based-on-the-edmx-file"></a>Para generar clases de Visual Basic basadas en el archivo .edmx

-   En el símbolo del sistema, ejecute el comando siguiente sin los saltos de línea:

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /in:Northwind.edmx /out:c:\northwind.vb
    ```

## <a name="see-also"></a>Vea también

- [Generar la biblioteca cliente del servicio de datos](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)
- [Cómo: Agregar una referencia de servicio de datos](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md)
- [Utilidad del cliente de servicio de datos de WCF (DataSvcUtil.exe)](../../../../docs/framework/data/wcf/wcf-data-service-client-utility-datasvcutil-exe.md)