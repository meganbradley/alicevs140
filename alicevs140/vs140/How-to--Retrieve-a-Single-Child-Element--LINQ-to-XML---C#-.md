---
title: "How to: Retrieve a Single Child Element (LINQ to XML) (C#)"
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
ms.assetid: ce37db9e-76fa-46eb-b4cc-e8f32d22ad90
caps.latest.revision: 5
---
# How to: Retrieve a Single Child Element (LINQ to XML) (C#)
This topic explains how to retrieve a single child element, given the name of the child element. When you know the name of the child element and that there is only one element that has this name, it can be convenient to retrieve just one element, instead of a collection.  
  
 The <xref:System.Xml.Linq.XContainer.Element?qualifyHint=False> method returns the first child <xref:System.Xml.Linq.XElement?qualifyHint=False> with the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.  
  
 If you want to retrieve a single child element in Visual Basic, a common approach is to use the XML property, and then retrieve the first element using array indexer notation.  
  
## Example  
 The following example demonstrates the use of the <xref:System.Xml.Linq.XContainer.Element?qualifyHint=False> method. This example takes the XML tree named `po` and finds the first element named `Comment`.  
  
 The Visual Basic example shows using array indexer notation to retrieve a single element.  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order (LINQ to XML)](../vs140/Sample-XML-File--Typical-Purchase-Order--LINQ-to-XML-1.md).  
  
```c#  
XElement po = XElement.Load("PurchaseOrder.xml");  
XElement e = po.Element("DeliveryNotes");  
Console.WriteLine(e);  
```  
  
 This example produces the following output:  
  
```xml  
  
<DeliveryNotes>Please leave packages in shed by driveway.</DeliveryNotes>  
```  
  
## Example  
 The following example shows the same code for XML that is in a namespace. For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order in a Namespace](../vs140/Sample-XML-File--Typical-Purchase-Order-in-a-Namespace1.md).  
  
```c#  
XElement po = XElement.Load("PurchaseOrderInNamespace.xml");  
XNamespace aw = "http://www.adventure-works.com";  
XElement e = po.Element(aw + "DeliveryNotes");  
Console.WriteLine(e);  
```  
  
 This example produces the following output:  
  
```xml  
  
<aw:DeliveryNotes xmlns:aw="http://www.adventure-works.com">Please leave packages in shed by driveway.</aw:DeliveryNotes>  
```  
  
## See Also  
 [LINQ to XML Axes (C#)](../vs140/LINQ-to-XML-Axes--C#-.md)