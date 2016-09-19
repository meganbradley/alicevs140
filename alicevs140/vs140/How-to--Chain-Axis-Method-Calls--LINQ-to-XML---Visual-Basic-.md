---
title: "How to: Chain Axis Method Calls (LINQ to XML) (Visual Basic)"
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
ms.assetid: e4e22942-39bd-460f-b3c0-9f09e53d3aa9
caps.latest.revision: 5
---
# How to: Chain Axis Method Calls (LINQ to XML) (Visual Basic)
A common pattern that you will use in your code is to call an axis method, then call one of the extension method axes.  
  
 There are two axes with the name of `Elements` that return a collection of elements: the <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=True> method and the <xref:System.Xml.Linq.Extensions.Elements?qualifyHint=True> method. You can combine these two axes to find all elements of a specified name at a given depth in the tree.  
  
## Example  
 This example uses <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=True> and <xref:System.Xml.Linq.Extensions.Elements?qualifyHint=True> to find all `Name` elements in all `Address` elements in all `PurchaseOrder` elements.  
  
 This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../vs140/Sample-XML-File--Multiple-Purchase-Orders--LINQ-to-XML-3.md).  
  
```vb  
Dim purchaseOrders As XElement = XElement.Load("PurchaseOrders.xml")  
Dim names As IEnumerable(Of XElement) = _  
    From el In purchaseOrders.<PurchaseOrder>.<Address>.<Name> _  
    Select el  
For Each e As XElement In names  
    Console.WriteLine(e)  
Next  
```  
  
 This example produces the following output:  
  
```  
<Name>Ellen Adams</Name>  
<Name>Tai Yee</Name>  
<Name>Cristian Osorio</Name>  
<Name>Cristian Osorio</Name>  
<Name>Jessica Arnold</Name>  
<Name>Jessica Arnold</Name>  
```  
  
 This works because one of the implementations of the `Elements` axis is as an extension method on <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XContainer?qualifyHint=False>. <xref:System.Xml.Linq.XElement?qualifyHint=False> derives from <xref:System.Xml.Linq.XContainer?qualifyHint=False>, so you can call the <xref:System.Xml.Linq.Extensions.Elements?qualifyHint=True> method on the results of a call to the <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=True> method.  
  
## Example  
 Sometimes you want to retrieve all elements at a particular element depth when there might or might not be intervening ancestors. For example, in the following document, you might want to retrieve all the `ConfigParameter` elements that are children of the `Customer` element, but not the `ConfigParameter` that is a child of the `Root` element.  
  
```xml  
<Root>  
  <ConfigParameter>RootConfigParameter</ConfigParameter>  
  <Customer>  
    <Name>Frank</Name>  
    <Config>  
      <ConfigParameter>FirstConfigParameter</ConfigParameter>  
    </Config>  
  </Customer>  
  <Customer>  
    <Name>Bob</Name>  
    <!--This customer doesn't have a Config element-->  
  </Customer>  
  <Customer>  
    <Name>Bill</Name>  
    <Config>  
      <ConfigParameter>SecondConfigParameter</ConfigParameter>  
    </Config>  
  </Customer>  
</Root>  
```  
  
 To do this, you can use the <xref:System.Xml.Linq.Extensions.Elements?qualifyHint=True> axis, as follows:  
  
```vb  
Dim root As XElement = XElement.Load("Irregular.xml")  
Dim configParameters As IEnumerable(Of XElement) = _  
    root.<Customer>.<Config>.<ConfigParameter>  
For Each cp As XElement In configParameters  
    Console.WriteLine(cp)  
Next  
```  
  
 This example produces the following output:  
  
```  
<ConfigParameter>FirstConfigParameter</ConfigParameter>  
<ConfigParameter>SecondConfigParameter</ConfigParameter>  
```  
  
## Example  
 The following example shows the same technique for XML that is in a namespace. For more information, see [Working with XML Namespaces (Visual Basic)](../Topic/Working%20with%20XML%20Namespaces%20\(Visual%20Basic\).md).  
  
 This example uses the following XML document: [Sample XML File: Multiple Purchase Orders in a Namespace](../vs140/Sample-XML-File--Multiple-Purchase-Orders-in-a-Namespace3.md).  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
  
Module Module1  
    Sub Main()  
        Dim purchaseOrders As XElement = XElement.Load("PurchaseOrdersInNamespace.xml")  
        Dim names As IEnumerable(Of XElement) = _  
            From el In purchaseOrders.<aw:PurchaseOrder>.<aw:Address>.<aw:Name> _  
            Select el  
        For Each e As XElement In names  
            Console.WriteLine(e)  
        Next  
    End Sub  
End Module  
```  
  
 This example produces the following output:  
  
```  
<aw:Name xmlns:aw="http://www.adventure-works.com">Ellen Adams</aw:Name>  
<aw:Name xmlns:aw="http://www.adventure-works.com">Tai Yee</aw:Name>  
<aw:Name xmlns:aw="http://www.adventure-works.com">Cristian Osorio</aw:Name>  
<aw:Name xmlns:aw="http://www.adventure-works.com">Cristian Osorio</aw:Name>  
<aw:Name xmlns:aw="http://www.adventure-works.com">Jessica Arnold</aw:Name>  
<aw:Name xmlns:aw="http://www.adventure-works.com">Jessica Arnold</aw:Name>  
```  
  
## See Also  
 [LINQ to XML Axes (Visual Basic)](../Topic/LINQ%20to%20XML%20Axes%20\(Visual%20Basic\).md)