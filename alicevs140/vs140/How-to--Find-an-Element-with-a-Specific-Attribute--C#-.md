---
title: "How to: Find an Element with a Specific Attribute (C#)"
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
ms.assetid: b92591aa-3cfb-490e-99f6-da8de335e362
caps.latest.revision: 5
---
# How to: Find an Element with a Specific Attribute (C#)
This topic shows how to find an element that has an attribute that has a specific value.  
  
## Example  
 The example shows how to find the `Address` element that has a `Type` attribute with a value of "Billing".  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order (LINQ to XML)](../vs140/Sample-XML-File--Typical-Purchase-Order--LINQ-to-XML-1.md).  
  
```c#  
XElement root = XElement.Load("PurchaseOrder.xml");  
IEnumerable<XElement> address =  
    from el in root.Elements("Address")  
    where (string)el.Attribute("Type") == "Billing"  
    select el;  
foreach (XElement el in address)  
    Console.WriteLine(el);  
```  
  
 This code produces the following output:  
  
```xml  
<Address Type="Billing">  
  <Name>Tai Yee</Name>  
  <Street>8 Oak Avenue</Street>  
  <City>Old Town</City>  
  <State>PA</State>  
  <Zip>95819</Zip>  
  <Country>USA</Country>  
</Address>  
```  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order in a Namespace](../vs140/Sample-XML-File--Typical-Purchase-Order-in-a-Namespace1.md).  
  
```c#  
XElement root = XElement.Load("PurchaseOrderInNamespace.xml");  
XNamespace aw = "http://www.adventure-works.com";  
IEnumerable<XElement> address =  
    from el in root.Elements(aw + "Address")  
    where (string)el.Attribute(aw + "Type") == "Billing"  
    select el;  
foreach (XElement el in address)  
    Console.WriteLine(el);  
```  
  
 This code produces the following output:  
  
```xml  
<aw:Address aw:Type="Billing" xmlns:aw="http://www.adventure-works.com">  
  <aw:Name>Tai Yee</aw:Name>  
  <aw:Street>8 Oak Avenue</aw:Street>  
  <aw:City>Old Town</aw:City>  
  <aw:State>PA</aw:State>  
  <aw:Zip>95819</aw:Zip>  
  <aw:Country>USA</aw:Country>  
</aw:Address>  
```  
  
## See Also  
 <xref:System.Xml.Linq.XElement.Attribute?qualifyHint=False>   
 <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=False>   
 [Basic Queries (LINQ to XML) (C#)](../Topic/Basic%20Queries%20\(LINQ%20to%20XML\)%20\(C%23\).md)   
 [Standard Query Operators Overview (C#)](../Topic/Standard%20Query%20Operators%20Overview%20\(C%23\).md)   
 [Projection Operations (C#)](../Topic/Projection%20Operations%20\(C%23\).md)