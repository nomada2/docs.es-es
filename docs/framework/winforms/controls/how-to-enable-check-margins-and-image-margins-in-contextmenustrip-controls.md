---
title: Procedimiento Habilitar los márgenes de comprobación y de imagen en los controles ContextMenuStrip
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ShowCheckMargin property [Windows Forms]
- ShowImageMargin property [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: eb584e71-59da-4012-aaca-dbe1c7c7a156
ms.openlocfilehash: 1193889523b2735f62b81bd1b001850f52d74dff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670269"
---
# <a name="how-to-enable-check-margins-and-image-margins-in-contextmenustrip-controls"></a>Procedimiento Habilitar los márgenes de comprobación y de imagen en los controles ContextMenuStrip
Puede personalizar los objetos <xref:System.Windows.Forms.ToolStripMenuItem> de su control <xref:System.Windows.Forms.MenuStrip> con marcas de verificación e imágenes personalizadas.  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo de código siguiente, se muestra cómo crear elementos de menú que tienen marcas de verificación e imágenes personalizadas.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#60](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#60)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#60](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#60)]  
  
 Establezca las propiedades <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A?displayProperty=nameWithType> y <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A?displayProperty=nameWithType> para especificar cuándo aparecerán las marcas de verificación y las imágenes personalizadas en los elementos de menú.  
  
## <a name="compiling-the-code"></a>Compilar el código  
 Para este ejemplo se necesita:  
  
-   Referencias a los ensamblados System.Design, System.Drawing y System.Windows.Forms.  
  
 Para obtener información sobre cómo compilar este ejemplo desde la línea de comandos para Visual Basic o Visual C#, vea [compilar desde la línea de comandos](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) o [de línea de comandos con csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). También puede compilar este ejemplo en Visual Studio pegando el código en un nuevo proyecto.  Consulte también [Cómo: Compilar y ejecutar un ejemplo de código completo de Windows Forms con Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Vea también
- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripDropDownMenu>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- [Control ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
