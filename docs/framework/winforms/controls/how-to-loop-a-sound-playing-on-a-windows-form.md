---
title: Procedimiento Repetir un sonido reproducido en un formulario de Windows
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sound loops
- SoundPlayer class [Windows Forms], play looping
- sounds [Windows Forms], looping
- playing sounds [Windows Forms], looping
ms.assetid: ea95dd46-10a3-46c0-8263-4b205f00df7f
ms.openlocfilehash: 93793fae418b33c954c9d597f020c8daf8cfedfd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493409"
---
# <a name="how-to-loop-a-sound-playing-on-a-windows-form"></a>Procedimiento Repetir un sonido reproducido en un formulario de Windows
En el ejemplo de código siguiente, se reproduce repetidamente un sonido. Cuando se ejecuta el código en el controlador de eventos `stopPlayingButton_Click`, todos los sonidos que se estén reproduciendo se detienen. Si no se está reproduciendo ningún sonido, no ocurre nada.  
  
## <a name="example"></a>Ejemplo  
 [!code-csharp[System.Media.SoundPlayer.PlayLooping#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.PlayLooping#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilar el código  
 Para este ejemplo se necesita:  
  
-   Referencias a los ensamblados System y System.Windows.Forms.  
  
-   Que reemplace el nombre de archivo `"c:\Windows\Media\chimes.wav"` por un nombre de archivo válido.  
  
 Para obtener información sobre cómo compilar este ejemplo desde la línea de comandos para visual Basic o Visual C#, vea [compilar desde la línea de comandos](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) o [de línea de comandos con csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). También puede compilar este ejemplo en Visual Studio pegando el código en un nuevo proyecto.  Consulte también [Cómo: Compilar y ejecutar un ejemplo de código completo de Windows Forms con Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="robust-programming"></a>Programación sólida  
 Las operaciones de archivo se deberían agregar dentro de los bloques de control de excepciones adecuados.  
  
 Las condiciones siguientes pueden provocar una excepción:  
  
-   El nombre de la ruta de acceso es incorrecto. Por ejemplo, contiene caracteres que no son válidos o es solo espacios en blanco (clase <xref:System.ArgumentException>).  
  
-   La ruta de acceso es de solo lectura (clase <xref:System.IO.IOException>).  
  
-   El nombre de la ruta de acceso es `Nothing` (clase <xref:System.ArgumentNullException>).  
  
-   El nombre de la ruta de acceso es demasiado largo (clase <xref:System.IO.PathTooLongException>).  
  
-   La ruta de acceso no es válida (clase <xref:System.IO.DirectoryNotFoundException>).  
  
-   La ruta de acceso es solo dos puntos ":" (clase <xref:System.NotSupportedException>).  
  
## <a name="net-framework-security"></a>Seguridad de .NET Framework  
 No tome ninguna decisión sobre el contenido del archivo basándose en su nombre. Por ejemplo, es posible que el archivo Form1.vb no sea un archivo de código fuente de Visual Basic. Compruebe todas las entradas antes de utilizar los datos en la aplicación.  
  
## <a name="see-also"></a>Vea también
- <xref:System.Media.SoundPlayer.PlayLooping%2A>
- [Cómo: Reproducir un sonido desde Windows Forms](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
- [Información general sobre la clase SoundPlayer](../../../../docs/framework/winforms/controls/soundplayer-class-overview.md)
