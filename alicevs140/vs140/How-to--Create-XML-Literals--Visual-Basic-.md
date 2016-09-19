---
title: "How to: Create XML Literals (Visual Basic)"
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
ms.assetid: 573a6db5-b14d-4e42-b356-8cc7e2d77745
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create XML Literals (Visual Basic)
You can create an XML document, fragment, or element directly in code by using an XML literal. The examples in this topic demonstrate how to create an XML element that has three child elements, and how to create an XML document.  
  
 You can also use the [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] APIs to create [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] objects. For more information, see <xref:System.Xml.Linq.XElement?qualifyHint=False>.  
  
### To create an XML element  
  
-   Create the XML inline by using the XML literal syntax, which is the same as the actual XML syntax.  
  
     [!CODE [VbXMLSamples#5](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#5)]  
  
     Run the code. The output of this code is:  
  
     `<contact>`  
  
     `<name>Patrick Hines</name>`  
  
     `<phone type="home">206-555-0144</phone>`  
  
     `<phone type="work">425-555-0145</phone>`  
  
     `</contact>`  
  
### To create an XML document  
  
-   Create the XML document inline. The following code creates an XML document that has literal syntax, an XML declaration, a processing instruction, a comment, and an element that contains another element.  
  
     [!CODE [VbXMLSamples#30](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#30)]  
  
     Run the code. The output of this code is:  
  
     `<?xml-stylesheet type="text/xsl" href="show_book.xsl"?>`  
  
     `<!-- Tests that the application works. -->`  
  
     `<books>`  
  
     `<book/>`  
  
     `</books>`  
  
## See Also  
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)   
 [Creating XML in Visual Basic](../vs140/Creating-XML-in-Visual-Basic.md)   
 [XML Element Literal](../Topic/XML%20Element%20Literal%20\(Visual%20Basic\).md)   
 [XML Document Literal](../Topic/XML%20Document%20Literal%20\(Visual%20Basic\).md)