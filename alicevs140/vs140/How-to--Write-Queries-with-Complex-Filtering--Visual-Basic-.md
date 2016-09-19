---
title: "How to: Write Queries with Complex Filtering (Visual Basic)"
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
ms.assetid: bf286ffc-7990-4b00-a4eb-ee3d70129950
caps.latest.revision: 5
---
# How to: Write Queries with Complex Filtering (Visual Basic)
Sometimes you want to write LINQ to XML queries with complex filters. For example, you might have to find all elements that have a child element with a particular name and value. This topic gives an example of writing a query with complex filtering.  
  
## Example  
 This example shows how to find all `PurchaseOrder` elements that have a child `Address` element that has a `Type` attribute equal to "Shipping" and a child `State` element equal to "NY". It uses a nested query in the `Where` clause, and the `Any` operator returns `True` if the collection has any elements in it.  
  
 This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../vs140/Sample-XML-File--Multiple-Purchase-Orders--LINQ-to-XML-3.md).  
  
 For more information about the `Any` operator, see [Quantifier Operations (Visual Basic)](../Topic/Quantifier%20Operations%20\(Visual%20Basic\).md).  
  
```vb  
Dim root As XElement = XElement.Load("PurchaseOrders.xml")  
Dim purchaseOrders As IEnumerable(Of XElement) = _  
    From el In root.<PurchaseOrder> _  
    Where _  
        (From add In el.<Address> _  
        Where _  
             add.@Type = "Shipping" And _  
             add.<State>.Value = "NY" _  
        Select add) _  
    .Any() _  
    Select el  
For Each el As XElement In purchaseOrders  
    Console.WriteLine(el.@PurchaseOrderNumber)  
Next  
```  
  
 This code produces the following output:  
  
```  
99505  
```  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (Visual Basic)](../Topic/Working%20with%20XML%20Namespaces%20\(Visual%20Basic\).md).  
  
 This example uses the following XML document: [Sample XML File: Multiple Purchase Orders in a Namespace](../vs140/Sample-XML-File--Multiple-Purchase-Orders-in-a-Namespace3.md).  
  
```vb  
Imports <xmlns:aw='http://www.adventure-works.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("PurchaseOrdersInNamespace.xml")  
        Dim purchaseOrders As IEnumerable(Of XElement) = _  
            From el In root.<aw:PurchaseOrder> _  
            Where _  
                (From add In el.<aw:Address> _  
                Where _  
                     add.@aw:Type = "Shipping" And _  
                     add.<aw:State>.Value = "NY" _  
                Select add) _  
            .Any() _  
            Select el  
        For Each el As XElement In purchaseOrders  
            Console.WriteLine(el.@aw:PurchaseOrderNumber)  
        Next  
    End Sub  
End Module  
```  
  
 This code produces the following output:  
  
```  
99505  
```  
  
## See Also  
 <xref:System.Xml.Linq.XElement.Attribute?qualifyHint=False>   
 <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=False>   
 [Basic Queries (LINQ to XML) (Visual Basic)](../vs140/Basic-Queries--LINQ-to-XML---Visual-Basic-.md)   
 [XML Child Axis Property](../Topic/XML%20Child%20Axis%20Property%20\(Visual%20Basic\).md)   
 [XML Attribute Axis Property](../Topic/XML%20Attribute%20Axis%20Property%20\(Visual%20Basic\).md)   
 [XML Value Property](../vs140/XML-Value-Property--Visual-Basic-.md)   
 [Projection Operations (Visual Basic)](../Topic/Projection%20Operations%20\(Visual%20Basic\).md)   
 [Quantifier Operations (Visual Basic)](../Topic/Quantifier%20Operations%20\(Visual%20Basic\).md)