---
title: "XML Literals Overview (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37987c15-4ab8-471b-bd45-399816bfb57f
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML Literals Overview (Visual Basic)
An *XML literal* allows you to incorporate XML directly into your [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] code. The XML literal syntax represents [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] objects, and it is the similar to the XML 1.0 syntax. This makes it easier to create XML elements and documents programmatically because your code has the same structure as the final XML.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiles XML literals into [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] objects. [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] provides a simple object model for creating and manipulating XML, and this model integrates well with [!INCLUDE[vbteclinqext](../vs140/includes/vbteclinqext_md.md)]. For more information, see <xref:System.Xml.Linq.XElement?qualifyHint=False>.  
  
 You can embed a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] expression in an XML literal. At run time, your application creates a [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] object for each literal, incorporating the values of the embedded expressions. This lets you specify dynamic content inside an XML literal. For more information, see [Embedded Expressions in XML](../Topic/Embedded%20Expressions%20in%20XML%20\(Visual%20Basic\).md).  
  
 For more information about the differences between the XML literal syntax and the XML 1.0 syntax, see [XML Literals and the XML 1.0 Specification](../vs140/XML-Literals-and-the-XML-1.0-Specification--Visual-Basic-.md).  
  
## Simple Literals  
 You can create a [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] object in your [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] code by typing or pasting in valid XML. An XML element literal returns an <xref:System.Xml.Linq.XElement?qualifyHint=False> object. For more information, see [XML Element Literal](../Topic/XML%20Element%20Literal%20\(Visual%20Basic\).md) and [XML Literals and the XML 1.0 Specification](../vs140/XML-Literals-and-the-XML-1.0-Specification--Visual-Basic-.md). The following example creates an XML element that has several child elements.  
  
 [!CODE [VbXMLSamples#5](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#5)]  
  
 You can create an XML document by starting an XML literal with `<?xml version="1.0"?>`, as shown in the following example. An XML document literal returns an <xref:System.Xml.Linq.XDocument?qualifyHint=False> object. For more information, see [XML Document Literal](../Topic/XML%20Document%20Literal%20\(Visual%20Basic\).md).  
  
 [!CODE [VbXMLSamples#6](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#6)]  
  
> [!NOTE]
>  The XML literal syntax in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] is not identical to the syntax in the XML 1.0 specification. For more information, see [XML Literals and the XML 1.0 Specification](../vs140/XML-Literals-and-the-XML-1.0-Specification--Visual-Basic-.md).  
  
## Line Continuation  
 An XML literal can span multiple lines without using line continuation characters (the space-underscore-enter sequence). This makes it easier to compare XML literals in code with XML documents.  
  
 The compiler treats line continuation characters as part of an XML literal. Therefore, you should use the space-underscore-enter sequence only when it belongs in the [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] object.  
  
 However, you do need line continuation characters if you have a multiline expression in an embedded expression. For more information, see [Embedded Expressions In XML](../Topic/Embedded%20Expressions%20in%20XML%20\(Visual%20Basic\).md).  
  
## Embedding Queries in XML Literals  
 You can use a query in an embedded expression. When you do this, the elements returned by the query are added to the XML element. This lets you add dynamic content, such as the result of a user's query, to an XML literal.  
  
 For example, the following code uses an embedded query to create XML elements from the members of the `phoneNumbers2` array and then add those elements as children of `contact2`.  
  
 [!CODE [VbXMLSamples#7](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#7)]  
  
## How the Compiler Creates Objects from XML Literals  
 The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler translates XML literals into calls to the equivalent [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] constructors to build up the [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] object. For example, the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler will translate the following code example into a call to the <xref:System.Xml.Linq.XProcessingInstruction?qualifyHint=False> constructor for the XML version instruction, calls to the <xref:System.Xml.Linq.XElement?qualifyHint=False> constructor for the `<contact>`, `<name>`, and `<phone>` elements, and calls to the <xref:System.Xml.Linq.XAttribute?qualifyHint=False> constructor for the `type` attribute. Specifically, given the attributes in the following sample, the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler will call the <xref:System.Xml.Linq.XAttribute.#ctor(System.Xml.Linq.XName,System.Object)?qualifyHint=False> constructor twice. The first will pass the value `type` for the `name` parameter and the value `home` for the `value` parameter. The second will also pass the value `type` for the `name` parameter, but the value `work` for the `value` parameter.  
  
 [!CODE [VbXMLSamples#6](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#6)]  
  
## See Also  
 <xref:System.Xml.Linq.XElement?qualifyHint=False>   
 [Creating XML in Visual Basic](../vs140/Creating-XML-in-Visual-Basic.md)   
 [Embedded Expressions in XML](../Topic/Embedded%20Expressions%20in%20XML%20\(Visual%20Basic\).md)   
 [XML Document Literal](../Topic/XML%20Document%20Literal%20\(Visual%20Basic\).md)   
 [XML Element Literal](../Topic/XML%20Element%20Literal%20\(Visual%20Basic\).md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)