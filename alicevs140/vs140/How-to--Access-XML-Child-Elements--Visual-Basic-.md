---
title: "How to: Access XML Child Elements (Visual Basic)"
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
ms.assetid: 6689eb36-c471-469f-a82d-099ab8197b25
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Access XML Child Elements (Visual Basic)
This example shows how to use a child axis property to access all XML child elements that have a specified name in an XML element. In particular, it uses the <xref:System.Xml.Linq.XElement.Value?qualifyHint=False> property to get the value of the first element in the collection that the `name` child axis property returns. The `name` child axis property gets all child elements named `phone` in the `contact` object. This example also uses the `phone` child axis property to access all child elements named `phone` that are contained in the `contact` object.  
  
## Example  
 [!CODE [VbXMLSamples#10](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#10)]  
  
## Compiling the Code  
 This example requires:  
  
-   A reference to the <xref:System.Xml.Linq?qualifyHint=False> namespace.  
  
## See Also  
 <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=True>   
 [XML Child Axis Property](../Topic/XML%20Child%20Axis%20Property%20\(Visual%20Basic\).md)   
 [XML Value Property](../vs140/XML-Value-Property--Visual-Basic-.md)   
 [Accessing XML Elements with Visual Basic](../vs140/Accessing-XML-in-Visual-Basic.md)   
 [Learning LINQ to XML Using Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)