---
title: "How to: Find an Attribute of the Parent (XPath-LINQ to XML) (Visual Basic)"
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
ms.assetid: 9d2572fd-27d4-426c-b079-16854cb9ec7d
caps.latest.revision: 5
---
# How to: Find an Attribute of the Parent (XPath-LINQ to XML) (Visual Basic)
This topic shows how to navigate to the parent element and find an attribute of it.  
  
 The XPath expression is:  
  
 `../@id`  
  
## Example  
 This example first finds an `Author` element. It then finds the `id` attribute of the parent element.  
  
 This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../vs140/Sample-XML-File--Books--LINQ-to-XML-3.md).  
  
```vb  
Dim books As XDocument = XDocument.Load("Books.xml")  
Dim author As XElement = books.Root.<Book>.<Author>.FirstOrDefault()  
  
' LINQ to XML query  
Dim att1 As XAttribute = author.Parent.Attribute("id")  
  
' XPath expression  
Dim att2 As XAttribute = DirectCast(author.XPathEvaluate("../@id"),  _  
    IEnumerable).Cast(Of XAttribute)().First()  
  
If att1 Is att2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(att1)  
  
```  
  
 This example produces the following output:  
  
```  
Results are identical  
id="bk101"  
```  
  
## See Also  
 [LINQ to XML for XPath Users (Visual Basic)](../Topic/LINQ%20to%20XML%20for%20XPath%20Users%20\(Visual%20Basic\).md)