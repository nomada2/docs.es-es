---
title: 'Carga de datos desde un archivo de texto para el procesamiento de aprendizaje automático: ML.NET'
description: Descubra cómo cargar datos de un archivo de texto para usarlos en la creación, el entrenamiento y la puntuación de modelos de Machine Learning con ML.NET
ms.date: 01/29/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 6a8f74cc5324050ca94e60592f083c35afc68377
ms.sourcegitcommit: dcc8feeff4718664087747529638ec9b47e65234
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/31/2019
ms.locfileid: "55479677"
---
# <a name="load-data-from-a-text-file-for-machine-learning-processing---mlnet"></a>Carga de datos desde un archivo de texto para el procesamiento de aprendizaje automático: ML.NET

`TextLoader` se usa para cargar datos de archivos de texto. Necesita especificar las columnas de datos, sus tipos y su ubicación en el archivo de texto.

Tenga en cuenta que es perfectamente aceptable leer algunas columnas de un archivo o la misma columna varias veces.

[Archivo de ejemplo](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt):

```console
Label   Workclass   education   marital-status
0   Private 11th    Never-married
0   Private HS-grad Married-civ-spouse
1   Local-gov   Assoc-acdm  Married-civ-spouse
1   Private Some-college    Married-civ-spouse
```

Para cargar los datos desde un archivo de texto:

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(
    columns: new TextLoader.Column[]
    {
        // A boolean column depicting the 'target label'.
        new TextLoader.Column("IsOver50k",DataKind.BL,0),
        // Three text columns.
        new TextLoader.Column("WorkClass",DataKind.TX,1),
        new TextLoader.Column("Education",DataKind.TX,2),
        new TextLoader.Column("MaritalStatus",DataKind.TX,3)
    },
    hasHeader: true
);

// Now read the file (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(dataPath);
```