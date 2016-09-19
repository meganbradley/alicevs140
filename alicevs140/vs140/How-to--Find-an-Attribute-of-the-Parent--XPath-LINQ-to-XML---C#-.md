---
title: "How to: Find an Attribute of the Parent (XPath-LINQ to XML) (C#)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbef9d89-a5c4-431f-80cc-7a2ebf323f86
caps.latest.revision: 5
---
# How to: Find an Attribute of the Parent (XPath-LINQ to XML) (C#)
This topic shows how to navigate to the parent element and find an attribute of it.  
  
 The XPath expression is:  
  
 `../@id`  
  
## Example  
 This example first finds an `Author` element. It then finds the `id` attribute of the parent element.  
  
 This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../vs140/Sample-XML-File--Books--LINQ-to-XML-1.md).  
  
```c#  
XDocument books = XDocument.Load("Books.xml");  
  
XElement author =   
    books  
    .Root  
    .Element("Book")  
    .Element("Author");  
  
// LINQ to XML query  
XAttribute att1 =  
    author  
    .Parent  
    .Attribute("id");  
  
// XPath expression  
XAttribute att2 = ((IEnumerable)author.XPathEvaluate("../@id")).Cast<XAttribute>().First();  
  
if (att1 == att2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(att1);  
```  
  
 This example produces the following output:  
  
```  
Results are identical  
id="bk101"  
```  
  
## See Also  
 [LINQ to XML for XPath Users (C#)](../vs140/LINQ-to-XML-for-XPath-Users--C#-.md)