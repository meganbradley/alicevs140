---
title: "Serializing with an XML Declaration (Visual Basic)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8726f79e-2bb0-4ba0-969d-197cca591647
caps.latest.revision: 3
---
# Serializing with an XML Declaration (Visual Basic)
This topic describes how to control whether serialization generates an XML declaration.  
  
## XML Declaration Generation  
 Serializing to a <xref:System.IO.File?qualifyHint=False> or a <xref:System.IO.TextWriter?qualifyHint=False> using the <xref:System.Xml.Linq.XElement.Save?qualifyHint=True> method or the <xref:System.Xml.Linq.XDocument.Save?qualifyHint=True> method generates an XML declaration. When you serialize to an <xref:System.Xml.XmlWriter?qualifyHint=False>, the writer settings (specified in an <xref:System.Xml.XmlWriterSettings?qualifyHint=False> object) determine whether an XML declaration is generated or not.  
  
 If you are serializing to a string using the `ToString` method, the resulting XML will not include an XML declaration.  
  
### Serializing with an XML Declaration  
 The following example creates an <xref:System.Xml.Linq.XElement?qualifyHint=False>, saves the document to a file, and then prints the file to the console:  
  
```vb  
Dim root As XElement = <Root>  
                           <Child>child content</Child>  
                       </Root>  
root.Save("Root.xml")  
Dim str As String = File.ReadAllText("Root.xml")  
Console.WriteLine(str)  
```  
  
 This example produces the following output:  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<Root>  
  <Child>child content</Child>  
</Root>  
```  
  
### Serializing without an XML Declaration  
 The following example shows how to save an <xref:System.Xml.Linq.XElement?qualifyHint=False> to an <xref:System.Xml.XmlWriter?qualifyHint=False>.  
  
```vb  
Dim sb As StringBuilder = New StringBuilder()  
Dim xws As XmlWriterSettings = New XmlWriterSettings()  
xws.OmitXmlDeclaration = True  
  
Using xw As XmlWriter = XmlWriter.Create(sb, xws)  
    Dim root = <Root>  
                   <Child>child content</Child>  
               </Root>  
    root.Save(xw)  
End Using  
Console.WriteLine(sb.ToString())  
```  
  
 This example produces the following output:  
  
```xml  
<Root><Child>child content</Child></Root>  
```  
  
## See Also  
 [Serializing XML Trees (Visual Basic)](../Topic/Serializing%20XML%20Trees%20\(Visual%20Basic\).md)