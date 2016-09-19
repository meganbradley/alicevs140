---
title: "How to: Calculate Intermediate Values (C#)"
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
ms.assetid: 7fd3001f-f8f9-4bce-879f-d4c7af8a04fe
caps.latest.revision: 5
---
# How to: Calculate Intermediate Values (C#)
This example shows how to calculate intermediate values that can be used in sorting, filtering, and selecting.  
  
## Example  
 The following example uses the `Let` clause.  
  
 This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../vs140/Sample-XML-File--Numerical-Data--LINQ-to-XML-3.md).  
  
```c#  
XElement root = XElement.Load("Data.xml");  
IEnumerable<decimal> extensions =  
    from el in root.Elements("Data")  
    let extension = (decimal)el.Element("Quantity") * (decimal)el.Element("Price")  
    where extension >= 25  
    orderby extension  
    select extension;  
foreach (decimal ex in extensions)  
    Console.WriteLine(ex);  
```  
  
 This code produces the following output:  
  
```  
55.92  
73.50  
89.99  
198.00  
435.00  
```  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
 This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../vs140/Sample-XML-File--Numerical-Data-in-a-Namespace3.md).  
  
```c#  
XElement root = XElement.Load("DataInNamespace.xml");  
XNamespace ad = "http://www.adatum.com";  
IEnumerable<decimal> extensions =  
    from el in root.Elements(ad + "Data")  
    let extension = (decimal)el.Element(ad + "Quantity") * (decimal)el.Element(ad + "Price")  
    where extension >= 25  
    orderby extension  
    select extension;  
foreach (decimal ex in extensions)  
    Console.WriteLine(ex);  
```  
  
 This code produces the following output:  
  
```  
55.92  
73.50  
89.99  
198.00  
435.00  
```  
  
## See Also  
 [Basic Queries (LINQ to XML) (C#)](../Topic/Basic%20Queries%20\(LINQ%20to%20XML\)%20\(C%23\).md)