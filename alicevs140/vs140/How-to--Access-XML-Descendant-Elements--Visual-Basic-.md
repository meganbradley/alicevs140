---
title: "How to: Access XML Descendant Elements (Visual Basic)"
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
ms.assetid: aabfa258-4112-4e7e-bab9-403f96072ef7
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Access XML Descendant Elements (Visual Basic)
This example shows how to use a descendant axis property to access all XML elements that have a specified name and that are contained under an XML element. In particular, it uses the `Value` property to get the value of the first element in the collection that the `name` descendant axis property returns. The `name` descendant axis property gets all elements named `name` that are contained in the `contacts` object. This example also uses the `phone` descendant axis property to access all descendants named `phone` that are contained in the `contacts` object.  
  
## Example  
 [!CODE [VbXMLSamples#31](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#31)]  
  
## Compiling the Code  
 This example requires:  
  
-   A reference to the <xref:System.Xml.Linq?qualifyHint=False> namespace.  
  
## See Also  
 <xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=True>   
 [XML Descendants Axis Property](../Topic/XML%20Descendant%20Axis%20Property%20\(Visual%20Basic\).md)   
 [XML Value Property](../vs140/XML-Value-Property--Visual-Basic-.md)   
 [Accessing XML Elements with Visual Basic](../vs140/Accessing-XML-in-Visual-Basic.md)   
 [Learning LINQ to XML Using Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)