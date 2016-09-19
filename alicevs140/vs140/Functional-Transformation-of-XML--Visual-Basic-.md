---
title: "Functional Transformation of XML (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdbe5b91-f457-4b4e-a11b-def4bdd77bab
caps.latest.revision: 5
---
# Functional Transformation of XML (Visual Basic)
This topic discusses the pure functional transformation approach to modifying XML documents, and contrasts it with a procedural approach.  
  
## Modifying an XML Document  
 One of the most common tasks for an XML programmer is transforming XML from one shape to another. The shape of an XML document is the structure of the document, which includes the following:  
  
-   The hierarchy expressed by the document.  
  
-   The element and attribute names.  
  
-   The data types of the elements and attributes.  
  
 In general, the most effective approach to transforming XML from one shape to another is that of pure functional transformation. In this approach, the primary programmer task is to create a transformation which is applied to the entire XML document (or to one or more strictly defined nodes). Functional transformation is arguably the easiest to code (after a programmer is familiar with the approach), yields the most maintainable code, and is often more compact than alternative approaches.  
  
### XML Functional Transformational Technologies  
 Microsoft offers two functional transformation technologies for use on XML documents: XSLT and LINQ to XML. XSLT is supported in the <xref:System.Xml.Xsl?qualifyHint=False> managed namespace and in the native COM implementation of MSXML. Although XSLT is a robust technology for manipulating XML documents, it requires expertise in a specialized domain, namely the XSLT language and its supporting APIs.  
  
 LINQ to XML provides the tools necessary to code pure functional transformations in an expressive and powerful way, within C# or Visual Basic code. For example, many of the examples in the LINQ to XML documentation use a pure functional approach. Also, in the [Tutorial: Manipulating Content in a WordprocessingML Document (Visual Basic)](../vs140/Tutorial--Manipulating-Content-in-a-WordprocessingML-Document--Visual-Basic-.md) tutorial, we use LINQ to XML in a functional approach to manipulate information in a Microsoft Word document.  
  
 For a more complete comparison of LINQ to XML with other Microsoft XML technologies, see [LINQ to XML vs. Other XML Technologies](../Topic/LINQ%20to%20XML%20vs.%20Other%20XML%20Technologies2.md).  
  
 XSLT is the recommended tool for  document-centric transformations when the source document has an irregular structure. However, LINQ to XML can also perform document-centric transforms. For more information, see [How to: Use Annotations to Transform LINQ to XML Trees in an XSLT Style (Visual Basic)](../Topic/How%20to:%20Use%20Annotations%20to%20Transform%20LINQ%20to%20XML%20Trees%20in%20an%20XSLT%20Style%20\(Visual%20Basic\).md).  
  
## See Also  
 [Introduction to Pure Functional Transformations (Visual Basic)](../vs140/Introduction-to-Pure-Functional-Transformations--Visual-Basic-.md)   
 [LINQ to XML vs. Other XML Technologies](../Topic/LINQ%20to%20XML%20vs.%20Other%20XML%20Technologies2.md)   
 [LINQ to XML vs. Other XML Technologies](../vs140/LINQ-to-XML-vs.-Other-XML-Technologies1.md)