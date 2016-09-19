---
title: "How to: Change the Namespace for an Entire XML Tree (Visual Basic)"
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
ms.assetid: 1837324b-5cb5-4fa8-95b9-3071efa0f913
caps.latest.revision: 5
---
# How to: Change the Namespace for an Entire XML Tree (Visual Basic)
You sometimes have to programmatically change the namespace for an element or an attribute. LINQ to XML makes this easy. The <xref:System.Xml.Linq.XElement.Name?qualifyHint=True> property can be set. The <xref:System.Xml.Linq.XAttribute.Name?qualifyHint=True> property cannot be set, but you can easily copy the attributes into a <xref:System.Collections.Generic.List`1?qualifyHint=True>, remove the existing attributes, and then add new attributes that are in the new desired namespace.  
  
 For more information, see [Working with XML Namespaces (Visual Basic)](../Topic/Working%20with%20XML%20Namespaces%20\(Visual%20Basic\).md).  
  
## Example  
 The following code creates two XML trees in no namespace. It then changes the namespace of each of the trees, and combines them into a single tree.  
  
```vb  
Dim tree1 As XElement = _  
    <Data>  
        <Child MyAttr="content">content</Child>  
    </Data>  
Dim tree2 As XElement = _  
    <Data>  
        <Child MyAttr="content">content</Child>  
    </Data>  
Dim aw As XNamespace = "http://www.adventure-works.com"  
Dim ad As XNamespace = "http://www.adatum.com"  
' change the namespace of every element and attribute in the first tree  
For Each el As XElement In tree1.DescendantsAndSelf  
    el.Name = aw.GetName(el.Name.LocalName)  
    Dim atList As List(Of XAttribute) = el.Attributes().ToList()  
    el.Attributes().Remove()  
    For Each at As XAttribute In atList  
        el.Add(New XAttribute(aw.GetName(at.Name.LocalName), at.Value))  
    Next  
Next  
' change the namespace of every element and attribute in the second tree  
For Each el As XElement In tree2.DescendantsAndSelf()  
    el.Name = ad.GetName(el.Name.LocalName)  
    Dim atList As List(Of XAttribute) = el.Attributes().ToList()  
    el.Attributes().Remove()  
    For Each at As XAttribute In atList  
        el.Add(New XAttribute(ad.GetName(at.Name.LocalName), at.Value))  
    Next  
Next  
' add attribute namespaces so that the tree will be serialized with  
' the aw and ad namespace prefixes  
tree1.Add( _  
    New XAttribute(XNamespace.Xmlns + "aw", "http://www.adventure-works.com") _  
)  
tree2.Add( _  
    New XAttribute(XNamespace.Xmlns + "ad", "http://www.adatum.com") _  
)  
' create a new composite tree  
Dim root As XElement = _  
    <Root>  
        <%= tree1 %>  
        <%= tree2 %>  
    </Root>  
Console.WriteLine(root)  
```  
  
 This example produces the following output:  
  
```xml  
<Root>  
  <aw:Data xmlns:aw="http://www.adventure-works.com">  
    <aw:Child aw:MyAttr="content">content</aw:Child>  
  </aw:Data>  
  <ad:Data xmlns:ad="http://www.adatum.com">  
    <ad:Child ad:MyAttr="content">content</ad:Child>  
  </ad:Data>  
</Root>  
```  
  
## See Also  
 [Modifying XML Trees (LINQ to XML) (Visual Basic)](../Topic/Modifying%20XML%20Trees%20\(LINQ%20to%20XML\)%20\(Visual%20Basic\).md)