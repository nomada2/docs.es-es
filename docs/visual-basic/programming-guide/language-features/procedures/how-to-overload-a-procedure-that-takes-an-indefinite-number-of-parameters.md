---
title: Procedimiento Sobrecargar un procedimiento que toma un número indefinido de parámetros (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], parameters
- procedure overloading [Visual Basic], indefinite number of parameters
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedure parameters
- procedures [Visual Basic], overloading
- procedures [Visual Basic], multiple versions
ms.assetid: c7042de2-2422-4039-94e8-ac298896af69
ms.openlocfilehash: 54a8a65db6e1f532cd21e36eeb5b98670efd4289
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506399"
---
# <a name="how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters-visual-basic"></a>Procedimiento Sobrecargar un procedimiento que toma un número indefinido de parámetros (Visual Basic)
Si un procedimiento tiene un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) parámetro, no se puede definir una versión sobrecargada que tome una matriz unidimensional de la matriz de parámetros. Para obtener más información, vea "Implícita sobrecargas de un parámetro ParamArray" en [consideraciones en sobrecarga de procedimientos](./considerations-in-overloading-procedures.md).  
  
### <a name="to-overload-a-procedure-that-takes-a-variable-number-of-parameters"></a>Sobrecargar un procedimiento que toma un número variable de parámetros  
  
1.  Confirmar que el procedimiento y llamar a código lógica beneficia sobrecargado versiones más de un `ParamArray` parámetro. Vea "Sobrecargas y ParamArray" en [consideraciones sobre la sobrecarga de procedimientos](./considerations-in-overloading-procedures.md).  
  
2.  Determinar qué número de valores proporcionados en la parte variable de la lista de parámetros debe aceptar el procedimiento. Esto podría incluir el caso de ningún valor y podría incluir el caso de una matriz unidimensional.  
  
3.  Para cada número aceptable de valores proporcionados, escribir un `Sub` o `Function` instrucción de declaración que define la lista de parámetros correspondientes. No use ninguno el `Optional` o `ParamArray` palabra clave en esta versión sobrecargada.  
  
4.  En cada declaración, anteponga la `Sub` o `Function` palabra clave con el [sobrecargas](../../../../visual-basic/language-reference/modifiers/overloads.md) palabra clave.  
  
5.  Después de cada declaración, escriba el código de procedimiento que se debe ejecutar cuando el código de llamada proporciona los valores correspondientes a la lista de parámetros de declaración.  
  
6.  Finalizar cada procedimiento con el `End Sub` o `End Function` instrucción según corresponda.  
  
## <a name="example"></a>Ejemplo  
 El ejemplo siguiente muestra un procedimiento definido con un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) parámetro y, a continuación, un conjunto equivalente de procedimientos sobrecargados.  
  
 [!code-vb[VbVbcnProcedures#69](./codesnippet/VisualBasic/how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters_1.vb)]  
  
 [!code-vb[VbVbcnProcedures#70](./codesnippet/VisualBasic/how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters_2.vb)]  
  
 No se puede sobrecargar un procedimiento con una lista de parámetros que toma una matriz unidimensional de la matriz de parámetros. Sin embargo, puede usar las firmas de las otras sobrecargas implícitas. Las declaraciones siguientes ilustran esto.  
  
 [!code-vb[VbVbcnProcedures#71](./codesnippet/VisualBasic/how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters_3.vb)]  
  
 El código en las versiones sobrecargadas no tiene que comprobar si el código de llamada proporciona uno o varios valores para el `ParamArray` parámetro, o si es así, cuántos. Visual Basic pasa el control a la versión que coincida con la lista de argumentos que realiza la llamada.  
  
## <a name="compiling-the-code"></a>Compilar el código  
 Dado que un procedimiento con un `ParamArray` parámetro es equivalente a un conjunto de versiones sobrecargadas, no se puede sobrecargar un procedimiento con una lista de parámetros correspondientes a cualquiera de estas sobrecargas implícitas. Para obtener más información, consulte [consideraciones en sobrecarga de procedimientos](./considerations-in-overloading-procedures.md).  
  
## <a name="net-framework-security"></a>Seguridad de .NET Framework  
 Si se trabaja con una matriz que puede ser excesivamente grande, hay un riesgo de sobrecargar alguna capacidad interna de la aplicación. Si acepta una matriz de parámetros, debe comprobar la longitud de la matriz el código de llamada pasado a él y seguir los pasos adecuados si es demasiado grande para la aplicación.  
  
## <a name="see-also"></a>Vea también
- [Procedimientos](./index.md)
- [Argumentos y parámetros de procedimiento](./procedure-parameters-and-arguments.md)
- [Parámetros opcionales](./optional-parameters.md)
- [Matrices de parámetros](./parameter-arrays.md)
- [Sobrecarga de procedimientos](./procedure-overloading.md)
- [Solución de problemas de procedimientos](./troubleshooting-procedures.md)
- [Cómo: Definir varias versiones de un procedimiento](./how-to-define-multiple-versions-of-a-procedure.md)
- [Cómo: Llamar a un procedimiento sobrecargado](./how-to-call-an-overloaded-procedure.md)
- [Cómo: Sobrecargar un procedimiento que toma parámetros opcionales](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [Resolución de sobrecargas](./overload-resolution.md)
