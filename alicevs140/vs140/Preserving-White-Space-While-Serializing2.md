---
title: "Preserving White Space While Serializing2"
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
H1: Preserving White Space While Serializing
ms.assetid: 2d7abbd4-37f4-422b-89dd-0a694b5edc17
caps.latest.revision: 5
---
# Preserving White Space While Serializing2
This topic describes how to control white space when serializing an XML tree.  
  
 A common scenario is to read indented XML, create an in-memory XML tree without any white space text nodes (that is, not preserving white space), perform some operations on the XML, and then save the XML with indentation. When you serialize the XML with formatting, only significant white space in the XML tree is preserved. This is the default behavior for [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)].  
  
 Another common scenario is to read and modify XML that has already been intentionally indented. You might not want to change this indentation in any way. To do this in [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)], you preserve white space when you load or parse the XML and disable formatting when you serialize the XML.  
  
## White Space Behavior of Methods that Serialize XML Trees  
 The following methods in the <xref:System.Xml.Linq.XElement?qualifyHint=False> and <xref:System.Xml.Linq.XDocument?qualifyHint=False> classes serialize an XML tree. You can serialize an XML tree to a file, a <xref:System.IO.TextReader?qualifyHint=False>, or an <xref:System.Xml.XmlReader?qualifyHint=False>. The `ToString` method serializes to a string.  
  
-   <xref:System.Xml.Linq.XElement.Save?qualifyHint=True>  
  
-   <xref:System.Xml.Linq.XDocument.Save?qualifyHint=True>  
  
-   <xref:System.Xml.Linq.XElement.ToString?qualifyHint=True>  
  
-   <xref:System.Xml.Linq.XDocument.ToString?qualifyHint=True>  
  
 If the method does not take <xref:System.Xml.Linq.SaveOptions?qualifyHint=False> as an argument, then the method will format (indent) the serialized XML. In this case, all insignificant white space in the XML tree is discarded.  
  
 If the method does take <xref:System.Xml.Linq.SaveOptions?qualifyHint=False> as an argument, then you can specify that the method not format (indent) the serialized XML. In this case, all white space in the XML tree is preserved.  
  
## See Also  
 [Serializing XML Trees (Visual Basic)](../Topic/Serializing%20XML%20Trees%20\(Visual%20Basic\).md)