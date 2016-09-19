---
title: "LINQ to XML Axes Overview (Visual Basic)"
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
ms.assetid: 9161f151-cfa8-4408-94ba-08a9ba3a486d
caps.latest.revision: 6
---
# LINQ to XML Axes Overview (Visual Basic)
After you have created an XML tree or loaded an XML document into an XML tree, you can query it to find elements and attributes and retrieve their values. You retrieve collections through the *axis methods*, also called *axes*. Some of the axes are methods in the <xref:System.Xml.Linq.XElement?qualifyHint=False> and <xref:System.Xml.Linq.XDocument?qualifyHint=False> classes that return <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> collections. Some of the axes are extension methods in the <xref:System.Xml.Linq.Extensions?qualifyHint=False> class. The axes that are implemented as extension methods operate on collections, and return collections.  
  
 As described in [XElement Class Overview](../vs140/XElement-Class-Overview.md), an <xref:System.Xml.Linq.XElement?qualifyHint=False> object represents a single element node. The content of an element can be complex (sometimes called structured content), or it can be a simple element. A simple element can be empty or can contain a value. If the node contains structured content, you can use the various axis methods to retrieve enumerations of descendant elements. The most commonly used axis methods are <xref:System.Xml.Linq.XContainer.Elements?qualifyHint=False> and <xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=False>.  
  
 In addition to the axis methods, which return collections, there are two more methods that you will commonly use in [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] queries. The <xref:System.Xml.Linq.XContainer.Element?qualifyHint=False> method returns a single <xref:System.Xml.Linq.XElement?qualifyHint=False>. The <xref:System.Xml.Linq.XElement.Attribute?qualifyHint=False> method returns a single <xref:System.Xml.Linq.XAttribute?qualifyHint=False>.  
  
 For many purposes, [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries provide the most powerful way to examine a tree, extract data from it, and transform it. [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries operate on objects that implement <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>, and the [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] axes return <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> collections, and <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XAttribute?qualifyHint=False> collections. You need these collections to perform your queries.  
  
 In addition to the axis methods that retrieve collections of elements and attributes, there are axis methods that allow you to iterate through the tree in great detail. For example, instead of dealing with elements and attributes, you can work with the nodes of the tree. Nodes are a finer level of granularity than elements and attributes. When working with nodes, you can examine XML comments, text nodes, processing instructions, and more. This functionality is important, for example, to someone who is writing a word processor and wants to save documents as XML. However, the majority of XML programmers are primarily concerned with elements, attributes, and their values.  
  
## Methods for Retrieving a Collection of Elements  
 The following is a summary of the methods of the <xref:System.Xml.Linq.XElement?qualifyHint=False> class (or its base classes) that you call on an <xref:System.Xml.Linq.XElement?qualifyHint=False> to return a collection of elements.  
  
|Method|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XNode.Ancestors?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the ancestors of this element. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the ancestors that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the descendants of this element. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the descendants that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XContainer.Elements?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the child elements of this element. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the child elements that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XNode.ElementsAfterSelf?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the elements that come after this element. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the elements after this element that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XNode.ElementsBeforeSelf?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the elements that come before this element. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the elements before this element that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XElement.AncestorsAndSelf?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of this element and its ancestors. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the elements that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XElement.DescendantsAndSelf?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of this element and its descendants. An overload returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False> of the elements that have the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
  
## Method for Retrieving a Single Element  
 The following method retrieves a single child from an <xref:System.Xml.Linq.XElement?qualifyHint=False> object.  
  
|Method|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XContainer.Element?qualifyHint=True>|Returns the first child <xref:System.Xml.Linq.XElement?qualifyHint=False> object that has the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
  
## Method for Retrieving a Collection of Attributes  
 The following method retrieves attributes from an <xref:System.Xml.Linq.XElement?qualifyHint=False> object.  
  
|Method|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XElement.Attributes?qualifyHint=True>|Returns an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XAttribute?qualifyHint=False> of all of the attributes.|  
  
## Method for Retrieving a Single Attribute  
 The following method retrieves a single attribute from an <xref:System.Xml.Linq.XElement?qualifyHint=False> object.  
  
|Method|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XElement.Attribute?qualifyHint=True>|Returns the <xref:System.Xml.Linq.XAttribute?qualifyHint=False> that has the specified <xref:System.Xml.Linq.XName?qualifyHint=False>.|  
  
## See Also  
 [LINQ to XML Axes (Visual Basic)](../Topic/LINQ%20to%20XML%20Axes%20\(Visual%20Basic\).md)