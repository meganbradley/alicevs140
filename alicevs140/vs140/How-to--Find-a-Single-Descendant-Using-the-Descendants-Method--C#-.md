---
title: "How to: Find a Single Descendant Using the Descendants Method (C#)"
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
ms.assetid: 6f735be9-0293-4680-8007-ca9d96bfebed
caps.latest.revision: 5
---
# How to: Find a Single Descendant Using the Descendants Method (C#)
You can use the <xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=False> axis method to quickly write code to find a single uniquely named element. This technique is especially useful when you want to find a particular descendant with a specific name. You could write the code to navigate to the desired element, but it is often faster and easier to write the code using the <xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=False> axis.  
  
## Example  
 This example uses the <xref:System.Linq.Enumerable.First?qualifyHint=False> standard query operator.  
  
```c#  
XElement root = XElement.Parse(@"<Root>  
  <Child1>  
    <GrandChild1>GC1 Value</GrandChild1>  
  </Child1>  
  <Child2>  
    <GrandChild2>GC2 Value</GrandChild2>  
  </Child2>  
  <Child3>  
    <GrandChild3>GC3 Value</GrandChild3>  
  </Child3>  
  <Child4>  
    <GrandChild4>GC4 Value</GrandChild4>  
  </Child4>  
</Root>");  
string grandChild3 = (string)  
    (from el in root.Descendants("GrandChild3")  
    select el).First();  
Console.WriteLine(grandChild3);  
```  
  
 This code produces the following output:  
  
```  
GC3 Value  
```  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
```c#  
XElement root = XElement.Parse(@"<aw:Root xmlns:aw='http://www.adventure-works.com'>  
  <aw:Child1>  
    <aw:GrandChild1>GC1 Value</aw:GrandChild1>  
  </aw:Child1>  
  <aw:Child2>  
    <aw:GrandChild2>GC2 Value</aw:GrandChild2>  
  </aw:Child2>  
  <aw:Child3>  
    <aw:GrandChild3>GC3 Value</aw:GrandChild3>  
  </aw:Child3>  
  <aw:Child4>  
    <aw:GrandChild4>GC4 Value</aw:GrandChild4>  
  </aw:Child4>  
</aw:Root>");  
XNamespace aw = "http://www.adventure-works.com";  
string grandChild3 = (string)  
    (from el in root.Descendants(aw + "GrandChild3")  
     select el).First();  
Console.WriteLine(grandChild3);  
```  
  
 This code produces the following output:  
  
```  
GC3 Value  
```  
  
## See Also  
 [Basic Queries (LINQ to XML) (C#)](../Topic/Basic%20Queries%20\(LINQ%20to%20XML\)%20\(C%23\).md)