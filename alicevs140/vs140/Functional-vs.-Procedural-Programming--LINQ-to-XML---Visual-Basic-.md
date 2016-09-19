---
title: "Functional vs. Procedural Programming (LINQ to XML) (Visual Basic)"
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
ms.assetid: ea1015a5-d4c8-4d79-8e1e-ba17a40a4f39
caps.latest.revision: 5
---
# Functional vs. Procedural Programming (LINQ to XML) (Visual Basic)
There are various types of XML applications:  
  
-   Some applications take source XML documents, and produce new XML documents that are in a different shape than the source documents.  
  
-   Some applications take source XML documents, and produce result documents in an entirely different form, such as HTML or CSV text files.  
  
-   Some applications take source XML documents, and insert records into a database.  
  
-   Some applications take data from another source, such as a database, and create XML documents from it.  
  
 These are not all of the types of XML applications, but these are a representative set of the types of functionality that an XML programmer has to implement.  
  
 With all of these types of applications, there are two contrasting approaches that a developer can take:  
  
-   Functional construction using a declarative approach.  
  
-   In-memory XML tree modification using procedural code.  
  
 LINQ to XML supports both approaches.  
  
 When using the functional approach, you write transformations that take the source documents and generate completely new result documents with the desired shape.  
  
 When modifying an XML tree in place, you write code that traverses and navigates through nodes in an in-memory XML tree, inserting, deleting, and modifying nodes as necessary.  
  
 You can use LINQ to XML with either approach. You use the same classes, and in some cases the same methods. However, the structure and goals of the two approaches are very different. For example, in different situations, one or the other approach will often have better performance, and use more or less memory. In addition, one or the other approach will be easier to write and yield more maintainable code.  
  
 To see the two approaches contrasted, see [In-Memory XML Tree Modification vs. Functional Construction (LINQ to XML) (Visual Basic)](../vs140/In-Memory-XML-Tree-Modification-vs.-Functional-Construction--LINQ-to-XML---Visual-Basic-.md).  
  
 For a tutorial on writing functional transformations, see [Pure Functional Transformations of XML (Visual Basic)](../vs140/Pure-Functional-Transformations-of-XML--Visual-Basic-.md).  
  
## See Also  
 [LINQ to XML Programming Overview (Visual Basic)](../vs140/LINQ-to-XML-Programming-Overview--Visual-Basic-.md)