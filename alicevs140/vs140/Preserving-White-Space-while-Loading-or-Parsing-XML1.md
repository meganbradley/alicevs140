---
title: "Preserving White Space while Loading or Parsing XML1"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Preserving White Space while Loading or Parsing XML
ms.assetid: f3ff58c4-55aa-4fcd-b933-e3a2ee6e706c
caps.latest.revision: 5
---
# Preserving White Space while Loading or Parsing XML1
This topic describes how to control the white space behavior of [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)].  
  
 A common scenario is to read indented XML, create an in-memory XML tree without any white space text nodes (that is, not preserving white space), perform some operations on the XML, and then save the XML with indentation. When you serialize the XML with formatting, only significant white space in the XML tree is preserved. This is the default behavior for [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)].  
  
 Another common scenario is to read and modify XML that has already been intentionally indented. You might not want to change this indentation in any way. To do this in [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)], you preserve white space when you load or parse the XML and disable formatting when you serialize the XML.  
  
 This topic describes the white space behavior of methods that populate XML trees. For information about controlling white space when you serialize XML trees, see [Preserving White Space While Serializing](../Topic/Preserving%20White%20Space%20While%20Serializing3.md).  
  
## Behavior of Methods that Populate XML Trees  
 The following methods in the <xref:System.Xml.Linq.XElement?qualifyHint=False> and <xref:System.Xml.Linq.XDocument?qualifyHint=False> classes populate an XML tree. You can populate an XML tree from a file, a <xref:System.IO.TextReader?qualifyHint=False>, an <xref:System.Xml.XmlReader?qualifyHint=False>, or a string:  
  
-   <xref:System.Xml.Linq.XElement.Load?qualifyHint=True>  
  
-   <xref:System.Xml.Linq.XElement.Parse?qualifyHint=True>  
  
-   <xref:System.Xml.Linq.XDocument.Load?qualifyHint=True>  
  
-   <xref:System.Xml.Linq.XDocument.Parse?qualifyHint=True>  
  
 If the method does not take <xref:System.Xml.Linq.LoadOptions?qualifyHint=False> as an argument, the method will not preserve insignificant white space.  
  
 In most cases, if the method takes <xref:System.Xml.Linq.LoadOptions?qualifyHint=False> as an argument, you can optionally preserve insignificant white space as text nodes in the XML tree. However, if the method is loading the XML from an <xref:System.Xml.XmlReader?qualifyHint=False>, then the <xref:System.Xml.XmlReader?qualifyHint=False> determines whether white space will be preserved or not. Setting <xref:System.Xml.Linq.LoadOptions.PreserveWhitespace?qualifyHint=False> will have no effect.  
  
 With these methods, if white space is preserved, insignificant white space is inserted into the XML tree as <xref:System.Xml.Linq.XText?qualifyHint=False> nodes. If white space is not preserved, text nodes are not inserted.  
  
 You can create an XML tree by using an <xref:System.Xml.XmlWriter?qualifyHint=False>. Nodes that are written to the <xref:System.Xml.XmlWriter?qualifyHint=False> are populated in the tree. However, when you build an XML tree using this method, all nodes are preserved, regardless of whether the node is white space or not, or whether the white space is significant or not.  
  
## See Also  
 [Parsing XML (C#)](../vs140/Parsing-XML--C#-.md)