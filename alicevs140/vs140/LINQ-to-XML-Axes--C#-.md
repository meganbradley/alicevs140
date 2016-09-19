---
title: "LINQ to XML Axes (C#)"
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
ms.assetid: 3f7d54ff-b608-43a1-9e2d-e70668b72df8
caps.latest.revision: 3
---
# LINQ to XML Axes (C#)
After you have created an XML tree or loaded an XML document into an XML tree, you can query it to find elements and attributes and retrieve their values.  
  
 Before you can write any queries, you must understand the [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] axes. There are two kinds of axis methods: First, there are the methods that you call on a single <xref:System.Xml.Linq.XElement?qualifyHint=False> object, <xref:System.Xml.Linq.XDocument?qualifyHint=False> object, or <xref:System.Xml.Linq.XNode?qualifyHint=False> object. These methods operate on a single object and return a collection of <xref:System.Xml.Linq.XElement?qualifyHint=False>, <xref:System.Xml.Linq.XAttribute?qualifyHint=False>, or <xref:System.Xml.Linq.XNode?qualifyHint=False> objects. Second, there are extension methods that operate on collections and return collections. The extension methods enumerate the source collection, call the appropriate axis method on each item in the collection, and concatenate the results.  
  
## In This Section  
  
|Topic|Description|  
|-----------|-----------------|  
|[LINQ to XML Axes Overview (C#)](../Topic/LINQ%20to%20XML%20Axes%20Overview%20\(C%23\).md)|Defines axes, and explains how they are used in the context of [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] queries.|  
|[How to: Retrieve a Collection of Elements (LINQ to XML) (C#)](../Topic/How%20to:%20Retrieve%20a%20Collection%20of%20Elements%20\(LINQ%20to%20XML\)%20\(C%23\).md)|Introduces the <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=False> method. This method retrieves a collection of the child elements of an element.|  
|[How to: Retrieve the Value of an Element (LINQ to XML) (C#)](../vs140/How-to--Retrieve-the-Value-of-an-Element--LINQ-to-XML---C#-.md)|Shows how to get the values of elements.|  
|[How to: Filter on Element Names (LINQ to XML) (C#)](../vs140/How-to--Filter-on-Element-Names--LINQ-to-XML---C#-.md)|Shows how to filter on element names when using axes.|  
|[How to: Chain Axis Method Calls (LINQ to XML) (C#)](../Topic/How%20to:%20Chain%20Axis%20Method%20Calls%20\(LINQ%20to%20XML\)%20\(C%23\).md)|Shows how to chain calls to axes methods.|  
|[How to: Retrieve a Single Child Element (LINQ to XML) (C#)](../vs140/How-to--Retrieve-a-Single-Child-Element--LINQ-to-XML---C#-.md)|Shows how to retrieve a single child element of an element, given the tag name of the child element.|  
|[How to: Retrieve a Collection of Attributes (LINQ to XML) (C#)](../vs140/How-to--Retrieve-a-Collection-of-Attributes--LINQ-to-XML---C#-.md)|Introduces the <xref:System.Xml.Linq.XElement.Attributes?qualifyHint=False> method. This method retrieves the attributes of an element.|  
|[How to: Retrieve a Single Attribute (LINQ to XML) (C#)](../vs140/How-to--Retrieve-a-Single-Attribute--LINQ-to-XML---C#-.md)|Shows how to retrieve a single attribute of an element, given the attribute name.|  
|[How to: Retrieve the Value of an Attribute (LINQ to XML) (C#)](../vs140/How-to--Retrieve-the-Value-of-an-Attribute--LINQ-to-XML---C#-.md)|Shows how to get the values of attributes.|  
|[How to: Retrieve the Shallow Value of an Element (C#)](../vs140/How-to--Retrieve-the-Shallow-Value-of-an-Element--C#-.md)|Shows how to retrieve the shallow value of an element.|  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [Programming Guide (LINQ to XML) (C#)](../Topic/Programming%20Guide%20\(LINQ%20to%20XML\)%20\(C%23\).md)