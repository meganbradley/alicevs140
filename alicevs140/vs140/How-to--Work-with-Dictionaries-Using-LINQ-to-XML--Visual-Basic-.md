---
title: "How to: Work with Dictionaries Using LINQ to XML (Visual Basic)"
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
ms.assetid: 6cb3f969-1986-414a-b850-87418712edea
caps.latest.revision: 5
---
# How to: Work with Dictionaries Using LINQ to XML (Visual Basic)
It is often convenient to convert varieties of data structures to XML, and XML back to other data structures. This topic shows a specific implementation of this general approach by converting a <xref:System.Collections.Generic.Dictionary`2?qualifyHint=False> to XML and back.  
  
## Example  
 This example uses XML literals and a query in an embedded expression. The query projects new <xref:System.Xml.Linq.XElement?qualifyHint=False> objects, which then become the new content for the `Root` <xref:System.Xml.Linq.XElement?qualifyHint=False> object.  
  
```vb  
Dim dict As Dictionary(Of String, String) = New Dictionary(Of String, String)()  
dict.Add("Child1", "Value1")  
dict.Add("Child2", "Value2")  
dict.Add("Child3", "Value3")  
dict.Add("Child4", "Value4")  
Dim root As XElement = _  
    <Root>  
        <%= From keyValue In dict _  
            Select New XElement(keyValue.Key, keyValue.Value) %>  
    </Root>  
Console.WriteLine(root)  
```  
  
 This code produces the following output:  
  
```xml  
  
          <Root>  
  <Child1>Value1</Child1>  
  <Child2>Value2</Child2>  
  <Child3>Value3</Child3>  
  <Child4>Value4</Child4>  
</Root>  
```  
  
## Example  
 The following code creates a dictionary from XML.  
  
```vb  
Dim root As XElement = _  
        <Root>  
            <Child1>Value1</Child1>  
            <Child2>Value2</Child2>  
            <Child3>Value3</Child3>  
            <Child4>Value4</Child4>  
        </Root>  
  
Dim dict As Dictionary(Of String, String) = New Dictionary(Of String, String)  
For Each el As XElement In root.Elements  
    dict.Add(el.Name.LocalName, el.Value)  
Next  
For Each str As String In dict.Keys  
    Console.WriteLine("{0}:{1}", str, dict(str))  
Next  
```  
  
 This code produces the following output:  
  
```  
Child1:Value1  
Child2:Value2  
Child3:Value3  
Child4:Value4  
```  
  
## See Also  
 [Projections and Transformations (LINQ to XML) (Visual Basic)](../vs140/Projections-and-Transformations--LINQ-to-XML---Visual-Basic-.md)