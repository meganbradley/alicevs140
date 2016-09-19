---
title: "How to: Calculate Intermediate Values (Visual Basic)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 933a97b2-dfe7-4f4d-94ad-e6e20df84abd
caps.latest.revision: 5
---
# How to: Calculate Intermediate Values (Visual Basic)
This example shows how to calculate intermediate values that can be used in sorting, filtering, and selecting.  
  
## Example  
 The following example uses the `Let` clause.  
  
 This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../vs140/Sample-XML-File--Numerical-Data--LINQ-to-XML-2.md).  
  
```vb  
Dim root As XElement = XElement.Load("Data.xml")  
Dim extensions As IEnumerable(Of Decimal) = _  
    From el In root.<Data> _  
    Let extension = CDec(el.<Quantity>.Value) * CDec(el.<Price>.Value) _  
    Where extension > 25 _  
    Order By extension _  
    Select extension  
For Each ex As Decimal In extensions  
    Console.WriteLine(ex)  
Next  
  
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
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (Visual Basic)](../Topic/Working%20with%20XML%20Namespaces%20\(Visual%20Basic\).md).  
  
 This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../vs140/Sample-XML-File--Numerical-Data-in-a-Namespace1.md).  
  
```vb  
Imports <xmlns="http://www.adatum.com">  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("DataInNamespace.xml")  
        Dim extensions As IEnumerable(Of Decimal) = _  
            From el In root.<Data> _  
            Let extension = CDec(el.<Quantity>.Value) * CDec(el.<Price>.Value) _  
            Where extension > 25 _  
            Order By extension _  
            Select extension  
        For Each ex As Decimal In extensions  
            Console.WriteLine(ex)  
        Next  
    End Sub  
End Module  
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
 [Basic Queries (LINQ to XML) (Visual Basic)](../vs140/Basic-Queries--LINQ-to-XML---Visual-Basic-.md)