---
title: "How to: Sort Elements (C#)"
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
ms.assetid: aee6fbbc-81fd-4b3e-b40f-6ed7b3bd3fee
caps.latest.revision: 5
---
# How to: Sort Elements (C#)
This example shows how to write a query that sorts its results.  
  
## Example  
 This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../vs140/Sample-XML-File--Numerical-Data--LINQ-to-XML-3.md).  
  
```c#  
XElement root = XElement.Load("Data.xml");  
IEnumerable<decimal> prices =  
    from el in root.Elements("Data")  
    let price = (decimal)el.Element("Price")  
    orderby price  
    select price;  
foreach (decimal el in prices)  
    Console.WriteLine(el);  
```  
  
 This code produces the following output:  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
 This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../vs140/Sample-XML-File--Numerical-Data-in-a-Namespace3.md).  
  
```c#  
XElement root = XElement.Load("DataInNamespace.xml");  
XNamespace aw = "http://www.adatum.com";  
IEnumerable<decimal> prices =  
    from el in root.Elements(aw + "Data")  
    let price = (decimal)el.Element(aw + "Price")  
    orderby price  
    select price;  
foreach (decimal el in prices)  
    Console.WriteLine(el);  
```  
  
 This code produces the following output:  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## See Also  
 [Sorting Data (C#)](../Topic/Sorting%20Data%20\(C%23\).md)   
 [Basic Queries (LINQ to XML) (C#)](../Topic/Basic%20Queries%20\(LINQ%20to%20XML\)%20\(C%23\).md)