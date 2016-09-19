---
title: "Removing Elements, Attributes, and Nodes from an XML Tree (Visual Basic)"
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
ms.assetid: 5cf21919-4360-4b49-b29d-58ea3164ac72
caps.latest.revision: 5
---
# Removing Elements, Attributes, and Nodes from an XML Tree (Visual Basic)
You can modify an XML tree, removing elements, attributes, and other types of nodes.  
  
 Removing a single element or a single attribute from an XML document is straightforward. However, when removing collections of elements or attributes, you should first materialize a collection into a list, and then delete the elements or attributes from the list. The best approach is to use the <xref:System.Xml.Linq.Extensions.Remove?qualifyHint=False> extension method, which will do this for you.  
  
 The main reason for doing this is that most of the collections you retrieve from an XML tree are yielded using deferred execution. If you do not first materialize them into a list, or if you do not use the extension methods, it is possible to encounter a certain class of bugs. For more information, see [Mixed Declarative Code/Imperative Code Bugs (LINQ to XML) (Visual Basic)](../Topic/Mixed%20Declarative%20Code-Imperative%20Code%20Bugs%20\(LINQ%20to%20XML\)%20\(Visual%20Basic\).md).  
  
 The following methods remove nodes and attributes from an XML tree.  
  
|Method|Description|  
|------------|-----------------|  
|[XAttribute.Remove](https://msdn.microsoft.com/en-us/library/system.xml.linq.xattribute.remove\(v=vs.110\).aspx)|Removes an <xref:System.Xml.Linq.XAttribute?qualifyHint=False> from its parent.|  
|[XContainer.RemoveNodes](https://msdn.microsoft.com/en-US/library/system.xml.linq.xcontainer.removenodes\(v=vs.110\).aspx)|Removes the child nodes from an <xref:System.Xml.Linq.XContainer?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XElement.RemoveAll?qualifyHint=True>|Removes content and attributes from an <xref:System.Xml.Linq.XElement?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XElement.RemoveAttributes?qualifyHint=True>|Removes the attributes of an <xref:System.Xml.Linq.XElement?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XElement.SetAttributeValue?qualifyHint=True>|If you pass `null` for value, then removes the attribute.|  
|<xref:System.Xml.Linq.XElement.SetElementValue?qualifyHint=True>|If you pass `null` for value, then removes the child element.|  
|<xref:System.Xml.Linq.XNode.Remove?qualifyHint=True>|Removes an <xref:System.Xml.Linq.XNode?qualifyHint=False> from its parent.|  
|<xref:System.Xml.Linq.Extensions.Remove?qualifyHint=True>|Removes every attribute or element in the source collection from its parent element.|  
  
## Example  
  
### Description  
 This example demonstrates three approaches to removing elements. First, it removes a single element. Second, it retrieves a collection of elements, materializes them using the <xref:System.Linq.Enumerable.ToList``1?qualifyHint=True> operator, and removes the collection. Finally, it retrieves a collection of elements and removes them using the <xref:System.Xml.Linq.Extensions.Remove?qualifyHint=False> extension method.  
  
 For more information on the <xref:System.Linq.Enumerable.ToList``1?qualifyHint=False> operator, see [Converting Data Types (Visual Basic)](../Topic/Converting%20Data%20Types%20\(Visual%20Basic\).md).  
  
### Code  
  
```vb  
Dim root As XElement = _  
    <Root>  
        <Child1>  
            <GrandChild1/>  
            <GrandChild2/>  
            <GrandChild3/>  
        </Child1>  
        <Child2>  
            <GrandChild4/>  
            <GrandChild5/>  
            <GrandChild6/>  
        </Child2>  
        <Child3>  
            <GrandChild7/>  
            <GrandChild8/>  
            <GrandChild9/>  
        </Child3>  
    </Root>  
root.<Child1>.<GrandChild1>.Remove()  
root.<Child2>.Elements().ToList().Remove()  
root.<Child3>.Elements().Remove()  
Console.WriteLine(root)  
  
```  
  
### Comments  
 This code produces the following output:  
  
```xml  
<Root>  
  <Child1>  
    <GrandChild2 />  
    <GrandChild3 />  
  </Child1>  
  <Child2 />  
  <Child3 />  
</Root>  
```  
  
 Notice that the first grandchild element has been removed from `Child1`. All grandchildren elements have been removed from `Child2` and from `Child3`.  
  
## See Also  
 [Modifying XML Trees (LINQ to XML) (Visual Basic)](../Topic/Modifying%20XML%20Trees%20\(LINQ%20to%20XML\)%20\(Visual%20Basic\).md)