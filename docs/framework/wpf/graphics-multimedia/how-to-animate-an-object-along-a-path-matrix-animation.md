---
title: Procedimiento Animar un objeto a lo largo de una trayectoria (animación de matriz)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (matrix animation)
- matrix animation [WPF]
ms.assetid: 7000e697-1414-468c-b915-cf66062fc49e
ms.openlocfilehash: 836f61e062b921c7e51166a35d8169f903fcbab9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738305"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation"></a>Procedimiento Animar un objeto a lo largo de una trayectoria (animación de matriz)
En este ejemplo se muestra cómo usar el <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> clase para animar un objeto a lo largo de una ruta de acceso que se define mediante un <xref:System.Windows.Media.PathGeometry>.  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se anima un objeto a lo largo de un trazado haciendo lo siguiente:  
  
-   Se aplica un <xref:System.Windows.Media.MatrixTransform> al objeto con el fin de moverla.  
  
-   Define la ruta de acceso mediante el uso de un <xref:System.Windows.Media.PathGeometry>.  
  
-   Crea un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> y lo usa para animar la <xref:System.Windows.Media.Matrix> propiedad de la <xref:System.Windows.Media.MatrixTransform>. El <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> toma el <xref:System.Windows.Media.PathGeometry> y lo usa para generar <xref:System.Windows.Media.Matrix> valores.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexample.xaml#matrixanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExample.cs#matrixanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExample.vb#matrixanimationusingpathwholepage)]  
  
 Para obtener un ejemplo completo, vea [ejemplo de animación de trazado](https://go.microsoft.com/fwlink/?LinkID=160028). Para obtener más información sobre los trazados geométricos, vea el [información general sobre geometría](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md).  
  
## <a name="see-also"></a>Vea también
- [Información general sobre animaciones](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Ejemplo de animación de trazado](https://go.microsoft.com/fwlink/?LinkID=160028)
- [Temas de procedimientos de animación de trazado](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
