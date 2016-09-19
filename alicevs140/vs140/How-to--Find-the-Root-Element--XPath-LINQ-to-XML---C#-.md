---
title: "How to: Find the Root Element (XPath-LINQ to XML) (C#)"
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
ms.assetid: 4fd824e0-4d39-429b-b092-f6a5c046ee6c
caps.latest.revision: 5
---
# How to: Find the Root Element (XPath-LINQ to XML) (C#)
This topic shows how to get the root element with XPath and [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)].  
  
 The XPath expression is:  
  
 `/PurchaseOrders`  
  
## Example  
 This example finds the root element.  
  
 This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../vs140/Sample-XML-File--Multiple-Purchase-Orders--LINQ-to-XML-2.md).  
  
```c#  
XDocument po = XDocument.Load("PurchaseOrders.xml");  
  
// LINQ to XML query  
XElement el1 = po.Root;  
  
// XPath expression  
XElement el2 = po.XPathSelectElement("/PurchaseOrders");  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1.Name);  
```  
  
 This example produces the following output:  
  
```  
Results are identical  
PurchaseOrders  
```  
  
## See Also  
 [LINQ to XML for XPath Users (C#)](../vs140/LINQ-to-XML-for-XPath-Users--C#-.md)