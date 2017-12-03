---
title: La clase XslTransform implementa el procesador XSLT
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 88373fe2-4a6b-44f9-8a62-8a3e348e3a46
caps.latest.revision: "6"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 167cd81ecbc25ca243e3b4a7a6aa7327679528e0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="xsltransform-class-implements-the-xslt-processor"></a><span data-ttu-id="30481-102">La clase XslTransform implementa el procesador XSLT</span><span class="sxs-lookup"><span data-stu-id="30481-102">XslTransform Class Implements the XSLT Processor</span></span>
> [!NOTE]
>  <span data-ttu-id="30481-103">La clase <xref:System.Xml.Xsl.XslTransform> es obsoleta en [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)].</span><span class="sxs-lookup"><span data-stu-id="30481-103">The <xref:System.Xml.Xsl.XslTransform> class is obsolete in the [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)].</span></span> <span data-ttu-id="30481-104">Puede llevar a cabo Extensible Stylesheet Language for Transformations (XSLT) mediante la clase <xref:System.Xml.Xsl.XslCompiledTransform>.</span><span class="sxs-lookup"><span data-stu-id="30481-104">You can perform Extensible Stylesheet Language for Transformations (XSLT) transformations using the <xref:System.Xml.Xsl.XslCompiledTransform> class.</span></span> <span data-ttu-id="30481-105">Vea [mediante la clase XslCompiledTransform](../../../../docs/standard/data/xml/using-the-xslcompiledtransform-class.md) y [Migrating From the XslTransform Class](../../../../docs/standard/data/xml/migrating-from-the-xsltransform-class.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="30481-105">See [Using the XslCompiledTransform Class](../../../../docs/standard/data/xml/using-the-xslcompiledtransform-class.md) and [Migrating From the XslTransform Class](../../../../docs/standard/data/xml/migrating-from-the-xsltransform-class.md) for more information.</span></span>  
  
 <span data-ttu-id="30481-106">La clase <xref:System.Xml.Xsl.XslTransform> es un procesador XSLT que implementa la recomendación de las transformaciones XSL (XSLT) versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="30481-106">The <xref:System.Xml.Xsl.XslTransform> class is an XSLT processor implementing the XSL Transformations (XSLT) Version 1.0 recommendation.</span></span> <span data-ttu-id="30481-107">El método <xref:System.Xml.Xsl.XslTransform.Load%2A> localiza y lee hojas de estilos y el método <xref:System.Xml.Xsl.XslTransform.Transform%2A> transforma el documento de origen determinado.</span><span class="sxs-lookup"><span data-stu-id="30481-107">The <xref:System.Xml.Xsl.XslTransform.Load%2A> method locates and reads style sheets, and the <xref:System.Xml.Xsl.XslTransform.Transform%2A> method transforms the given source document.</span></span> <span data-ttu-id="30481-108">Cualquier almacén que implemente la interfaz <xref:System.Xml.XPath.IXPathNavigable> puede utilizarse como documento de origen para la transformación <xref:System.Xml.Xsl.XslTransform>.</span><span class="sxs-lookup"><span data-stu-id="30481-108">Any store that implements the <xref:System.Xml.XPath.IXPathNavigable> interface can be used as the source document for the <xref:System.Xml.Xsl.XslTransform>.</span></span> <span data-ttu-id="30481-109">El [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] implementa actualmente la interfaz <xref:System.Xml.XPath.IXPathNavigable> en <xref:System.Xml.XmlDocument>, <xref:System.Xml.XmlDataDocument>, y <xref:System.Xml.XPath.XPathDocument>, de manera que todos estos pueden utilizarse como documento de origen de entrada para una transformación.</span><span class="sxs-lookup"><span data-stu-id="30481-109">The [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] currently implements the <xref:System.Xml.XPath.IXPathNavigable> interface on the <xref:System.Xml.XmlDocument>, the <xref:System.Xml.XmlDataDocument>, and the <xref:System.Xml.XPath.XPathDocument>, so all of these can be used as the input source document to a transformation.</span></span>  
  
 <span data-ttu-id="30481-110">El objeto <xref:System.Xml.Xsl.XslTransform> en [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] solamente admite la especificación XSLT 1.0, definida con el siguiente espacio de nombres:</span><span class="sxs-lookup"><span data-stu-id="30481-110">The <xref:System.Xml.Xsl.XslTransform> object in the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] only supports the XSLT 1.0 specification, defined with the following namespace:</span></span>  
  
```xml  
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">    
```  
  
 <span data-ttu-id="30481-111">La hoja de estilos puede cargarse utilizando el método <xref:System.Xml.Xsl.XslTransform.Load%2A>, desde cualquiera de las clases siguientes:</span><span class="sxs-lookup"><span data-stu-id="30481-111">The style sheet can be loaded, using the <xref:System.Xml.Xsl.XslTransform.Load%2A> method, from one of the following classes:</span></span>  
  
-   <span data-ttu-id="30481-112">XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="30481-112">XPathNavigator</span></span>  
  
-   <span data-ttu-id="30481-113">XmlReader</span><span class="sxs-lookup"><span data-stu-id="30481-113">XmlReader</span></span>  
  
-   <span data-ttu-id="30481-114">Una cadena que representa una dirección URL</span><span class="sxs-lookup"><span data-stu-id="30481-114">A string representing a URL</span></span>  
  
 <span data-ttu-id="30481-115">Existe un método <xref:System.Xml.Xsl.XslTransform.Load%2A> distinto para cada una de las clases de entrada citadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="30481-115">There is a different <xref:System.Xml.Xsl.XslTransform.Load%2A> method for each of the above input classes.</span></span> <span data-ttu-id="30481-116">Algunos métodos toman una combinación de una de estas clases y la clase <xref:System.Xml.XmlResolver> como argumentos.</span><span class="sxs-lookup"><span data-stu-id="30481-116">Some methods take in a combination of one of these classes and the <xref:System.Xml.XmlResolver> class as arguments.</span></span> <span data-ttu-id="30481-117"><xref:System.Xml.XmlResolver> localiza los recursos a los que hace referencia `<xsl:import>` o `<xsl:include>` y que se encuentran en la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="30481-117">The <xref:System.Xml.XmlResolver> locates resources referenced by `<xsl:import>` or `<xsl:include>` found in the style sheet.</span></span> <span data-ttu-id="30481-118">Los métodos siguientes toman una cadena <xref:System.Xml.XmlReader> o <xref:System.Xml.XPath.XPathNavigator> como entrada.</span><span class="sxs-lookup"><span data-stu-id="30481-118">The following methods take a string, <xref:System.Xml.XmlReader>, or <xref:System.Xml.XPath.XPathNavigator> as input.</span></span>  
  
```vb  
Overloads Public Sub Load(String)  
```  
  
```csharp  
public void Load(string);  
```  
  
```vb  
Overloads Public Sub Load(String, XmlResolver)  
```  
  
```csharp  
public void Load(string, XmlResolver);  
```  
  
```vb  
Overloads Public Sub Load(XmlReader, XmlResolver, Evidence)  
```  
  
```csharp  
public void Load(XmlReader, XmlResolver, Evidence);  
```  
  
```vb  
Overloads Public Sub Load(XPathNavigator, XmlResolver, Evidence)  
```  
  
```csharp  
public void Load(XPathNavigator, XmlResolver, Evidence);  
```  
  
 <span data-ttu-id="30481-119">La mayoría de los métodos <xref:System.Xml.Xsl.XslTransform.Load%2A> que se han mostrado antes toman un <xref:System.Xml.XmlResolver> como parámetro.</span><span class="sxs-lookup"><span data-stu-id="30481-119">Most of the <xref:System.Xml.Xsl.XslTransform.Load%2A> methods shown above take an <xref:System.Xml.XmlResolver> as a parameter.</span></span> <span data-ttu-id="30481-120"><xref:System.Xml.XmlResolver> se utiliza para cargar la hoja de estilos y cualquier hoja u hojas de estilos a las que se haga referencia en los elementos xsl:import y xsl:include.</span><span class="sxs-lookup"><span data-stu-id="30481-120">The <xref:System.Xml.XmlResolver> is used to load the style sheet and any style sheet(s) referenced in xsl:import and xsl:include elements.</span></span>  
  
 <span data-ttu-id="30481-121">La mayoría de los métodos <xref:System.Xml.Xsl.XslTransform.Load%2A> toman también Evidence como parámetro.</span><span class="sxs-lookup"><span data-stu-id="30481-121">Most of the <xref:System.Xml.Xsl.XslTransform.Load%2A> methods also take evidence as a parameter.</span></span> <span data-ttu-id="30481-122">El parámetro evidence es el <xref:System.Security.Policy.Evidence> que está asociado con la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="30481-122">The evidence parameter is the <xref:System.Security.Policy.Evidence> that is associated with the style sheet.</span></span> <span data-ttu-id="30481-123">El nivel de seguridad de la hoja de estilos afecta al nivel de seguridad de cualquier recurso posterior al que haga referencia la hoja de estilos como, por ejemplo, los scripts que contenga, cualquier función `document()` que utilice y cualquier objeto de extensión utilizado por <xref:System.Xml.Xsl.XsltArgumentList>.</span><span class="sxs-lookup"><span data-stu-id="30481-123">The security level of the style sheet affects the security level of any subsequent resources it references, such as the script it contains, any `document()` functions it uses, and any extension objects used by the <xref:System.Xml.Xsl.XsltArgumentList>.</span></span>  
  
 <span data-ttu-id="30481-124">Si la hoja de estilos se ha cargado utilizando un método <xref:System.Xml.Xsl.XslTransform.Load%2A> que contiene un parámetro URL y no hay ninguna evidencia, la evidencia de la hoja de estilos se calcula combinando la dirección URL dada con su sitio y zona.</span><span class="sxs-lookup"><span data-stu-id="30481-124">If the style sheet is loaded using a <xref:System.Xml.Xsl.XslTransform.Load%2A> method that contains a URL parameter and no evidence is provided, the evidence of the style sheet is calculated by combining the given URL with its site and zone.</span></span>  
  
 <span data-ttu-id="30481-125">Si no se proporciona ningún identificador URI, la hoja de estilos se convierte en un parámetro de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="30481-125">If no URI or evidence is provided, then the evidence set for the style sheet is fully trusted.</span></span> <span data-ttu-id="30481-126">No cargue hojas de estilos desde orígenes que no sean de confianza ni agregue objetos de extensión que no sean de confianza en <xref:System.Xml.Xsl.XsltArgumentList>.</span><span class="sxs-lookup"><span data-stu-id="30481-126">Do not load style sheets from untrusted sources, or add untrusted extension objects into the <xref:System.Xml.Xsl.XsltArgumentList>.</span></span>  
  
 <span data-ttu-id="30481-127">Para obtener más información sobre los niveles de seguridad y evidencia y cómo afecta a secuencias de comandos, consulte [XSLT Stylesheet Scripting mediante \<msxsl: script >](../../../../docs/standard/data/xml/xslt-stylesheet-scripting-using-msxsl-script.md).</span><span class="sxs-lookup"><span data-stu-id="30481-127">For more information about security levels and evidence and how it affects scripting, see [XSLT Stylesheet Scripting Using \<msxsl:script>](../../../../docs/standard/data/xml/xslt-stylesheet-scripting-using-msxsl-script.md).</span></span> <span data-ttu-id="30481-128">Para obtener información sobre los niveles de seguridad y evidencia y cómo afecta a los objetos de extensión, vea [XsltArgumentList para parámetros Stylesheet y objetos de extensión](../../../../docs/standard/data/xml/xsltargumentlist-for-style-sheet-parameters-and-extension-objects.md).</span><span class="sxs-lookup"><span data-stu-id="30481-128">For information about security levels and evidence and how it affects extension objects, see [XsltArgumentList for Style Sheet Parameters and Extension Objects](../../../../docs/standard/data/xml/xsltargumentlist-for-style-sheet-parameters-and-extension-objects.md).</span></span>  
  
 <span data-ttu-id="30481-129">Para obtener información sobre los niveles de seguridad y evidencia y cómo afecta a la `document()` función, vea [resolver hojas de estilos XSLT externo y documentos](../../../../docs/standard/data/xml/resolving-external-xslt-style-sheets-and-documents.md).</span><span class="sxs-lookup"><span data-stu-id="30481-129">For information about security levels and evidence and how it affects the `document()` function, see [Resolving External XSLT Style Sheets and Documents](../../../../docs/standard/data/xml/resolving-external-xslt-style-sheets-and-documents.md).</span></span>  
  
 <span data-ttu-id="30481-130">Una hoja de estilos se puede suministrar con varios parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="30481-130">A style sheet can be supplied with a number of input parameters.</span></span> <span data-ttu-id="30481-131">Asimismo puede llamar también a funciones en objetos de extensión.</span><span class="sxs-lookup"><span data-stu-id="30481-131">The style sheet can also call functions on extension objects.</span></span> <span data-ttu-id="30481-132">Tanto los parámetros como los objetos de extensión se suministran a la hoja de estilos mediante la clase <xref:System.Xml.Xsl.XsltArgumentList>.</span><span class="sxs-lookup"><span data-stu-id="30481-132">Both parameters and extension objects are supplied to the style sheet using the <xref:System.Xml.Xsl.XsltArgumentList> class.</span></span> <span data-ttu-id="30481-133">Para obtener más información acerca de <xref:System.Xml.Xsl.XsltArgumentList>, vea <xref:System.Xml.Xsl.XsltArgumentList>.</span><span class="sxs-lookup"><span data-stu-id="30481-133">For more information about the <xref:System.Xml.Xsl.XsltArgumentList>, see <xref:System.Xml.Xsl.XsltArgumentList>.</span></span>  
  
## <a name="recommended-secure-use-of-xsltransform-class"></a><span data-ttu-id="30481-134">Uso seguro recomendado de la clase XslTransform</span><span class="sxs-lookup"><span data-stu-id="30481-134">Recommended Secure Use of XslTransform Class</span></span>  
 <span data-ttu-id="30481-135">Los privilegios de seguridad de la hoja de estilos dependen de la evidencia proporcionada.</span><span class="sxs-lookup"><span data-stu-id="30481-135">The security privileges of the style sheet depend on the evidence provided.</span></span> <span data-ttu-id="30481-136">En la siguiente tabla se resume la ubicación de la hoja de estilos y se ofrece una explicación del tipo de evidencia que hay que dar.</span><span class="sxs-lookup"><span data-stu-id="30481-136">The following table summarizes the location of the style sheet and gives an explanation of what type of evidence to give.</span></span>  
  
-   <span data-ttu-id="30481-137">La hoja de estilos XSLT no tiene referencias externas o proviene de un código base en el que confía.</span><span class="sxs-lookup"><span data-stu-id="30481-137">The XSLT style sheet has no external references, or the style sheet comes from a code base that you trust.</span></span>  
  
    -   <span data-ttu-id="30481-138">Proporcione la evidencia desde el ensamblado:</span><span class="sxs-lookup"><span data-stu-id="30481-138">Provide the evidence from your assembly:</span></span>  
  
         `Dim xslt = New XslTransform() xslt.Load(stylesheet, resolver, Me.GetType().Assembly.Evidence)`  
  
         `XsltTransform xslt = new XslTransform();  xslt.Load(stylesheet, resolver, this.GetType().Assembly.Evidence);`  
  
-   <span data-ttu-id="30481-139">La hoja de estilos XSLT proviene de un código fuente exterior.</span><span class="sxs-lookup"><span data-stu-id="30481-139">The XSLT style sheet comes from an outside source.</span></span> <span data-ttu-id="30481-140">Se conoce el origen del código fuente y existe un identificador URI que se puede comprobar.</span><span class="sxs-lookup"><span data-stu-id="30481-140">The origin of the source is known and there is a verifiable URI.</span></span>  
  
    -   <span data-ttu-id="30481-141">Cree la evidencia utilizando el identificador URI.</span><span class="sxs-lookup"><span data-stu-id="30481-141">Create evidence using the URI.</span></span>  
  
         `Dim xslt As New XslTransform() Dim ev As Evidence = XmlSecureResolver.CreateEvidenceForUrl(stylesheetUri) xslt.Load(stylesheet, resolver, evidence)`  
  
         `XslTransform xslt = new XslTransform(); Evidence ev = XmlSecureResolver.CreateEvidenceForUrl(stylesheetUri); xslt.Load(stylesheet, resolver, evidence);`  
  
-   <span data-ttu-id="30481-142">La hoja de estilos XSLT proviene de un código fuente exterior.</span><span class="sxs-lookup"><span data-stu-id="30481-142">The XSLT style sheet comes from an outside source.</span></span> <span data-ttu-id="30481-143">Se desconoce el origen del código fuente.</span><span class="sxs-lookup"><span data-stu-id="30481-143">The origin of the source is not known.</span></span>  
  
    -   <span data-ttu-id="30481-144">Establezca la evidencia en `null`.</span><span class="sxs-lookup"><span data-stu-id="30481-144">Set evidence to `null`.</span></span> <span data-ttu-id="30481-145">No se procesan los bloques de scripts, no se admite la función `document()` de XSLT y no están permitidos los objetos de extensión privilegiada.</span><span class="sxs-lookup"><span data-stu-id="30481-145">Script blocks are not processed, the XSLT `document()` function is not supported, and privileged extension objects are disallowed.</span></span>  
  
         <span data-ttu-id="30481-146">Además, también puede establecer el parámetro `resolver` en una referencia `null`, lo que garantiza que los elementos `xsl:import` y `xsl:include` no se procesan.</span><span class="sxs-lookup"><span data-stu-id="30481-146">Additionally, you can also set the `resolver` parameter to `null` This ensures that `xsl:import` and `xsl:include` elements are not processed.</span></span>  
  
-   <span data-ttu-id="30481-147">La hoja de estilos XSLT proviene de un código fuente exterior.</span><span class="sxs-lookup"><span data-stu-id="30481-147">The XSLT style sheet comes from an outside source.</span></span> <span data-ttu-id="30481-148">Se desconoce el origen del código fuente, pero es necesaria la compatibilidad con los scripts.</span><span class="sxs-lookup"><span data-stu-id="30481-148">The origin of the source is not known, but you require script support.</span></span>  
  
    -   <span data-ttu-id="30481-149">Solicite la evidencia al llamador.</span><span class="sxs-lookup"><span data-stu-id="30481-149">Request evidence from the caller.</span></span>  
  
## <a name="transformation-of-xml-data"></a><span data-ttu-id="30481-150">Transformación de datos XML</span><span class="sxs-lookup"><span data-stu-id="30481-150">Transformation of XML Data</span></span>  
 <span data-ttu-id="30481-151">Una vez cargada la hoja de estilos, la transformación comienza con la llamada a uno de los métodos <xref:System.Xml.Xsl.XslTransform.Transform%2A> y con el suministro de un documento de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="30481-151">Once a style sheet is loaded, the transformation starts by calling one of the <xref:System.Xml.Xsl.XslTransform.Transform%2A> methods and supplying an input source document.</span></span> <span data-ttu-id="30481-152">El método <xref:System.Xml.Xsl.XslTransform.Transform%2A> se sobrecarga para proporcionar diferentes salidas de transformación.</span><span class="sxs-lookup"><span data-stu-id="30481-152">The <xref:System.Xml.Xsl.XslTransform.Transform%2A> method is overloaded to provide different transformation outputs.</span></span> <span data-ttu-id="30481-153">La transformación puede producir los siguientes formatos de salida:</span><span class="sxs-lookup"><span data-stu-id="30481-153">The transformation can result in the following output formats:</span></span>  
  
-   <xref:System.Xml.XmlReader>  
  
-   <xref:System.Xml.XmlWriter>  
  
-   <xref:System.IO.TextWriter>  
  
-   <xref:System.IO.Stream>  
  
-   <span data-ttu-id="30481-154">Dirección URL de cadena de archivo</span><span class="sxs-lookup"><span data-stu-id="30481-154">String URL of file</span></span>  
  
 <span data-ttu-id="30481-155">Este último formato, la dirección URL de cadena, proporciona una situación utilizada comúnmente en la transformación de un documento de entrada que se encuentra en una dirección URL y escribe el documento en la dirección URL de salida.</span><span class="sxs-lookup"><span data-stu-id="30481-155">This last format, the string URL, provides for a commonly used scenario in transforming an input document located in a URL and writing the document to the output URL.</span></span> <span data-ttu-id="30481-156">Este método <xref:System.Xml.Xsl.XslTransform.Transform%2A> es útil para cargar un documento XML desde un archivo, realizar la transformación XSLT y escribir la salida en un archivo.</span><span class="sxs-lookup"><span data-stu-id="30481-156">This <xref:System.Xml.Xsl.XslTransform.Transform%2A> method is a convenience method to load an XML document from a file, perform the XSLT transformation, and write the output to a file.</span></span> <span data-ttu-id="30481-157">De esta forma se evita tener que crear y cargar el documento de origen de entrada y después escribirlo en una secuencia de archivo.</span><span class="sxs-lookup"><span data-stu-id="30481-157">This prevents you from having to create and load the input source document, and then write to a file stream.</span></span> <span data-ttu-id="30481-158">En el ejemplo de código siguiente se muestra este uso del método <xref:System.Xml.Xsl.XslTransform.Transform%2A> con la dirección URL de cadena como entrada y como salida:</span><span class="sxs-lookup"><span data-stu-id="30481-158">The following code sample shows this use of the <xref:System.Xml.Xsl.XslTransform.Transform%2A> method using the string URL as input and output:</span></span>  
  
```vb  
Dim xsltransform As XslTransform = New XslTransform()  
xsltransform.Load("favorite.xsl")  
xsltransform.Transform("MyDocument.Xml", "TransformResult.xml", Nothing)  
```  
  
```csharp  
XslTransform xsltransform = new XslTransform();  
xsltransform.Load("favorite.xsl");  
xsltransform.Transform("MyDocument.xml", "TransformResult.xml", null);  
```  
  
## <a name="transforming-a-section-of-an-xml-document"></a><span data-ttu-id="30481-159">Transformar una sección de un documento XML</span><span class="sxs-lookup"><span data-stu-id="30481-159">Transforming a Section of an XML Document</span></span>  
 <span data-ttu-id="30481-160">Las transformaciones se aplican al documento en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="30481-160">Transformations apply to the document as a whole.</span></span> <span data-ttu-id="30481-161">En otras palabras, si se pasa un nodo distinto del nodo raíz del documento, esto no evita que el proceso de transformación pueda obtener acceso a todos los nodos del documento cargado.</span><span class="sxs-lookup"><span data-stu-id="30481-161">In other words, if you pass in a node other than the document root node, this does not prevent the transformation process from accessing all nodes in the loaded document.</span></span> <span data-ttu-id="30481-162">Para transformar un fragmento del árbol de resultados, habrá que crear un <xref:System.Xml.XmlDocument> que contenga el fragmento de árbol de resultados y pasar ese <xref:System.Xml.XmlDocument> al método <xref:System.Xml.Xsl.XslTransform.Transform%2A>.</span><span class="sxs-lookup"><span data-stu-id="30481-162">To transform a result tree fragment, you must create an <xref:System.Xml.XmlDocument> containing just the result tree fragment and pass that <xref:System.Xml.XmlDocument> to the <xref:System.Xml.Xsl.XslTransform.Transform%2A> method.</span></span> <span data-ttu-id="30481-163">En el ejemplo siguiente se realiza una transformación en un fragmento de árbol de resultados.</span><span class="sxs-lookup"><span data-stu-id="30481-163">The following example performs a transformation on a result tree fragment.</span></span>  
  
```vb  
Dim xslt As New XslTransform()  
xslt.Load("print_root.xsl")  
Dim doc As New XmlDocument()  
doc.Load("library.xml")  
' Create a new document containing just the result tree fragment.  
Dim testNode As XmlNode = doc.DocumentElement.FirstChild  
Dim tmpDoc As New XmlDocument()  
tmpDoc.LoadXml(testNode.OuterXml)  
' Pass the document containing the result tree fragment   
' to the Transform method.  
Console.WriteLine(("Passing " + tmpDoc.OuterXml + " to print_root.xsl"))  
xslt.Transform(tmpDoc, Nothing, Console.Out, Nothing)  
```  
  
```csharp  
XslTransform xslt = new XslTransform();       
xslt.Load("print_root.xsl");  
XmlDocument doc = new XmlDocument();  
doc.Load("library.xml");  
// Create a new document containing just the result tree fragment.  
XmlNode testNode = doc.DocumentElement.FirstChild;   
XmlDocument tmpDoc = new XmlDocument();   
tmpDoc.LoadXml(testNode.OuterXml);  
// Pass the document containing the result tree fragment   
// to the Transform method.  
Console.WriteLine("Passing " + tmpDoc.OuterXml + " to print_root.xsl");  
xslt.Transform(tmpDoc, null, Console.Out, null);  
```  
  
 <span data-ttu-id="30481-164">En el ejemplo se han utilizado los archivos library.xml y print_root.xsl como entrada y el resultado que se muestra en la consola es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="30481-164">The example uses the library.xml and print_root.xsl files as input and outputs the following to the console.</span></span>  
  
```  
Passing <book genre="novel" ISBN="1-861001-57-5"><title>Pride And Prejudice</title></book> to print_root.xsl   
Root node is book.  
```  
  
 <span data-ttu-id="30481-165">library.xml</span><span class="sxs-lookup"><span data-stu-id="30481-165">library.xml</span></span>  
  
```xml  
<library>  
  <book genre='novel' ISBN='1-861001-57-5'>  
     <title>Pride And Prejudice</title>  
  </book>  
  <book genre='novel' ISBN='1-81920-21-2'>  
     <title>Hook</title>  
  </book>  
</library>  
```  
  
 <span data-ttu-id="30481-166">print_root.xsl</span><span class="sxs-lookup"><span data-stu-id="30481-166">print_root.xsl</span></span>  
  
```xml  
<stylesheet version="1.0" xmlns="http://www.w3.org/1999/XSL/Transform" >  
  <output method="text" />   
  <template match="/">  
     Root node is  <value-of select="local-name(//*[position() = 1])" />   
  </template>  
</stylesheet>  
```  
  
## <a name="migration-of-xslt-from-net-framework-version-10-to-net-framework-version-11"></a><span data-ttu-id="30481-167">Migración de XSLT de la versión 1.0 a la versión 1.1 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="30481-167">Migration of XSLT from .NET Framework version 1.0 to .NET Framework version 1.1</span></span>  
 <span data-ttu-id="30481-168">La tabla siguiente muestra los métodos versión 1.0 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] obsoletos y los nuevos métodos versión 1.1 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] para el método <xref:System.Xml.Xsl.XslTransform.Load%2A>.</span><span class="sxs-lookup"><span data-stu-id="30481-168">The following table shows the obsolete [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] version 1.0 methods and new [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] version 1.1 methods for the <xref:System.Xml.Xsl.XslTransform.Load%2A> method.</span></span> <span data-ttu-id="30481-169">Los nuevos métodos permiten limitar los permisos de la hoja de estilos especificando la evidencia.</span><span class="sxs-lookup"><span data-stu-id="30481-169">The new methods enable you to limit the permissions of the style sheet by specifying evidence.</span></span>  
  
|<span data-ttu-id="30481-170">Métodos de .NET Framework versión 1.0 Load obsoletos</span><span class="sxs-lookup"><span data-stu-id="30481-170">Obsolete .NET Framework version 1.0 Load Methods</span></span>|<span data-ttu-id="30481-171">Métodos Load de reemplazo .NET Framework versión 1.1</span><span class="sxs-lookup"><span data-stu-id="30481-171">Replacement .NET Framework version 1.1 Load Methods</span></span>|  
|------------------------------------------------------|---------------------------------------------------------|  
|<span data-ttu-id="30481-172">Load(entrada XPathNavigator);</span><span class="sxs-lookup"><span data-stu-id="30481-172">Load(XPathNavigator input);</span></span><br /><br /> <span data-ttu-id="30481-173">Load(entrada XPathNavigator, resolución XmlResolver);</span><span class="sxs-lookup"><span data-stu-id="30481-173">Load(XPathNavigator input, XmlResolver resolver);</span></span>|<span data-ttu-id="30481-174">Load(hoja de estilos XPathNavigator, resolución XmlResolver, evidencia Evidence);</span><span class="sxs-lookup"><span data-stu-id="30481-174">Load(XPathNavigator stylesheet, XmlResolver resolver, Evidence evidence);</span></span>|  
|<span data-ttu-id="30481-175">Load(hoja de estilos IXPathNavigable);</span><span class="sxs-lookup"><span data-stu-id="30481-175">Load(IXPathNavigable stylesheet);</span></span><br /><br /> <span data-ttu-id="30481-176">Load(hoja de estilos IXPathNavigable, resolución XmlResolver);</span><span class="sxs-lookup"><span data-stu-id="30481-176">Load(IXPathNavigable stylesheet, XmlResolver resolver);</span></span>|<span data-ttu-id="30481-177">Load(hoja de estilos IXPathNavigable, resolución XmlResolver, evidencia Evidence);</span><span class="sxs-lookup"><span data-stu-id="30481-177">Load(IXPathNavigable stylesheet, XmlResolver resolver, Evidence evidence);</span></span>|  
|<span data-ttu-id="30481-178">Load(hoja de estilos XmlReader);</span><span class="sxs-lookup"><span data-stu-id="30481-178">Load(XmlReader stylesheet);</span></span><br /><br /> <span data-ttu-id="30481-179">Load(hoja de estilos XmlReader, resolución XmlResolver);</span><span class="sxs-lookup"><span data-stu-id="30481-179">Load(XmlReader stylesheet, XmlResolver resolver);</span></span>|<span data-ttu-id="30481-180">Load(hoja de estilos XmlReader, resolución XmlResolver, evidencia Evidence);</span><span class="sxs-lookup"><span data-stu-id="30481-180">Load(XmlReader stylesheet, XmlResolver resolver, Evidence evidence);</span></span>|  
  
 <span data-ttu-id="30481-181">La tabla siguiente muestra los métodos obsoletos y nuevos <xref:System.Xml.Xsl.XslTransform.Transform%2A>.</span><span class="sxs-lookup"><span data-stu-id="30481-181">The following table shows the obsolete and new methods for the <xref:System.Xml.Xsl.XslTransform.Transform%2A> method.</span></span> <span data-ttu-id="30481-182">Los nuevos métodos toman un objeto <xref:System.Xml.XmlResolver>.</span><span class="sxs-lookup"><span data-stu-id="30481-182">The new methods take an <xref:System.Xml.XmlResolver> object.</span></span>  
  
|<span data-ttu-id="30481-183">Métodos de .NET Framework versión 1.0 Transform obsoletos</span><span class="sxs-lookup"><span data-stu-id="30481-183">Obsolete .NET Framework version 1.0 Transform Methods</span></span>|<span data-ttu-id="30481-184">Versión de .NET Framework métodos 1.1 Transform de reemplazo</span><span class="sxs-lookup"><span data-stu-id="30481-184">Replacement .NET Framework version Transform 1.1 Methods</span></span>|  
|-----------------------------------------------------------|--------------------------------------------------------------|  
|<span data-ttu-id="30481-185">XmlReader Transform(entrada XPathNavigator, argumentos XsltArgumentList)</span><span class="sxs-lookup"><span data-stu-id="30481-185">XmlReader Transform(XPathNavigator input, XsltArgumentList args)</span></span>|<span data-ttu-id="30481-186">XmlReader Transform(entrada XPathNavigator, argumentos XsltArgumentList, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-186">XmlReader Transform(XPathNavigator  input, XsltArgumentList args, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-187">XmlReader Transform(entrada IXPathNavigable, argumentos XsltArgumentList)</span><span class="sxs-lookup"><span data-stu-id="30481-187">XmlReader Transform(IXPathNavigable input, XsltArgumentList args)</span></span>|<span data-ttu-id="30481-188">XmlReader Transform(entrada IXPathNavigable, argumentos XsltArgumentList, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-188">XmlReader Transform(IXPathNavigable input, XsltArgumentList args, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-189">Void Transform(entrada XPathNavigator, argumentos XsltArgumentList, salida XmlWriter)</span><span class="sxs-lookup"><span data-stu-id="30481-189">Void Transform(XPathNavigator input, XsltArgumentList args, XmlWriter output)</span></span>|<span data-ttu-id="30481-190">Void Transform(entrada XPathNavigator, argumentos XsltArgumentList, salida XmlWriter, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-190">Void Transform(XPathNavigator input, XsltArgumentList args, XmlWriter output, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-191">Void Transform(entrada IXPathNavigable, argumentos XsltArgumentList, salida XmlWriter)</span><span class="sxs-lookup"><span data-stu-id="30481-191">Void Transform(IXPathNavigable input, XsltArgumentList args, XmlWriter output)</span></span>|<span data-ttu-id="30481-192">Void Transform(entrada IXpathNavigable, argumentos XsltArgumentList, salida XmlWriter, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-192">Void Transform(IXpathNavigable input, XsltArgumentList args, XmlWriter output, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-193">Void Transform(entrada XPathNavigator, argumentos XsltArgumentList, salida TextWriter)</span><span class="sxs-lookup"><span data-stu-id="30481-193">Void Transform(XPathNavigator input, XsltArgumentList args, TextWriter output)</span></span>|<span data-ttu-id="30481-194">Void Transform(entrada XPathNavigator, argumentos XsltArgumentList, salida TextWriter, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-194">Void Transform(XPathNavigator input, XsltArgumentList args, TextWriter output, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-195">Void Transform(entrada IXPathNavigable, argumentos XsltArgumentList, salida TextWriter)</span><span class="sxs-lookup"><span data-stu-id="30481-195">Void Transform(IXPathNavigable input, XsltArgumentList args, TextWriter output)</span></span>|<span data-ttu-id="30481-196">Void Transform(entrada IXPathNavigable, argumentos XsltArgumentList, salida TextWriter, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-196">Void Transform(IXPathNavigable input, XsltArgumentList args, TextWriter output, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-197">Void Transform(entrada XPathNavigator, argumentos XsltArgumentList, salida Stream)</span><span class="sxs-lookup"><span data-stu-id="30481-197">Void Transform(XPathNavigator input, XsltArgumentList args, Stream output)</span></span>|<span data-ttu-id="30481-198">Void Transform(entrada XPathNavigator, argumentos XsltArgumentList, salida Stream, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-198">Void Transform(XPathNavigator input, XsltArgumentList args, Stream output, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-199">Void Transform(entrada IXPathNavigable, argumentos XsltArgumentList, salida Stream)</span><span class="sxs-lookup"><span data-stu-id="30481-199">Void Transform(IXPathNavigable input, XsltArgumentList args, Stream output)</span></span>|<span data-ttu-id="30481-200">Void Transform(entrada IXPathNavigable, argumentos XsltArgumentList, salida Stream, resolución XmlResolver)</span><span class="sxs-lookup"><span data-stu-id="30481-200">Void Transform(IXPathNavigable input, XsltArgumentList args, Stream output, XmlResolver resolver)</span></span>|  
|<span data-ttu-id="30481-201">Void Transform(entrada String, salida String);</span><span class="sxs-lookup"><span data-stu-id="30481-201">Void Transform(String input, String output);</span></span>|<span data-ttu-id="30481-202">Void Transform(entrada String, salida String, resolución XmlResolver);</span><span class="sxs-lookup"><span data-stu-id="30481-202">Void Transform(String input, String output, XmlResolver resolver);</span></span>|  
  
 <span data-ttu-id="30481-203">La propiedad <xref:System.Xml.Xsl.XslTransform.XmlResolver%2A?displayProperty=nameWithType> es obsoleta en [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] versión 1.1.</span><span class="sxs-lookup"><span data-stu-id="30481-203">The <xref:System.Xml.Xsl.XslTransform.XmlResolver%2A?displayProperty=nameWithType> property is obsolete in [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] version 1.1.</span></span> <span data-ttu-id="30481-204">En su lugar, use la nueva <xref:System.Xml.Xsl.XslTransform.Transform%2A> sobrecargas que toman un <xref:System.Xml.XmlResolver> objeto.</span><span class="sxs-lookup"><span data-stu-id="30481-204">Instead, use the new <xref:System.Xml.Xsl.XslTransform.Transform%2A> overloads which take an <xref:System.Xml.XmlResolver> object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30481-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="30481-205">See Also</span></span>  
 <xref:System.Xml.Xsl.XslTransform>  
 [<span data-ttu-id="30481-206">Transformaciones XSLT con la clase XslTransform</span><span class="sxs-lookup"><span data-stu-id="30481-206">XSLT Transformations with the XslTransform Class</span></span>](../../../../docs/standard/data/xml/xslt-transformations-with-the-xsltransform-class.md)  
 [<span data-ttu-id="30481-207">XPathNavigator en transformaciones</span><span class="sxs-lookup"><span data-stu-id="30481-207">XPathNavigator in Transformations</span></span>](../../../../docs/standard/data/xml/xpathnavigator-in-transformations.md)  
 [<span data-ttu-id="30481-208">XPathNodeIterator en transformaciones</span><span class="sxs-lookup"><span data-stu-id="30481-208">XPathNodeIterator in Transformations</span></span>](../../../../docs/standard/data/xml/xpathnodeiterator-in-transformations.md)  
 [<span data-ttu-id="30481-209">Entrada XPathDocument Input para XslTransform</span><span class="sxs-lookup"><span data-stu-id="30481-209">XPathDocument Input to XslTransform</span></span>](../../../../docs/standard/data/xml/xpathdocument-input-to-xsltransform.md)  
 [<span data-ttu-id="30481-210">Entrada de XmlDataDocument en XslTransform</span><span class="sxs-lookup"><span data-stu-id="30481-210">XmlDataDocument Input to XslTransform</span></span>](../../../../docs/standard/data/xml/xmldatadocument-input-to-xsltransform.md)  
 [<span data-ttu-id="30481-211">Entrada de XmlDocument en XslTransform</span><span class="sxs-lookup"><span data-stu-id="30481-211">XmlDocument Input to XslTransform</span></span>](../../../../docs/standard/data/xml/xmldocument-input-to-xsltransform.md)