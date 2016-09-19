---
title: "How to: Debug Empty Query Results Sets (C#)"
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
ms.assetid: b569f0dc-425e-45a6-acbf-770fb761c981
caps.latest.revision: 5
---
# How to: Debug Empty Query Results Sets (C#)
One of the most common problems when querying XML trees is that if the XML tree has a default namespace, the developer sometimes writes the query as though the XML were not in a namespace.  
  
 The first set of examples in this topic shows a typical way that XML in a default namespace is loaded, and is queried improperly.  
  
 The second set of examples show the necessary corrections so that you can query XML in a namespace.  
  
 For more information, see [Working with XML Namespaces (C#)](../Topic/Working%20with%20XML%20Namespaces%20\(C%23\).md).  
  
## Example  
 This example shows creation of XML in a namespace, and a query that returns an empty result set.  
  
```c#  
XElement root = XElement.Parse(  
@"<Root xmlns='http://www.adventure-works.com'>  
    <Child>1</Child>  
    <Child>2</Child>  
    <Child>3</Child>  
    <AnotherChild>4</AnotherChild>  
    <AnotherChild>5</AnotherChild>  
    <AnotherChild>6</AnotherChild>  
</Root>");  
IEnumerable<XElement> c1 =  
    from el in root.Elements("Child")  
    select el;  
Console.WriteLine("Result set follows:");  
foreach (XElement el in c1)  
    Console.WriteLine((int)el);  
Console.WriteLine("End of result set");  
```  
  
 This example produces the following result:  
  
```  
Result set follows:  
End of result set  
```  
  
## Example  
 This example shows creation of XML in a namespace, and a query that is coded properly.  
  
 The solution is to declare and initialize an <xref:System.Xml.Linq.XNamespace?qualifyHint=False> object, and to use it when specifying <xref:System.Xml.Linq.XName?qualifyHint=False> objects. In this case, the argument to the <xref:System.Xml.Linq.XElement.Elements?qualifyHint=False> method is an <xref:System.Xml.Linq.XName?qualifyHint=False> object.  
  
```c#  
XElement root = XElement.Parse(  
@"<Root xmlns='http://www.adventure-works.com'>  
    <Child>1</Child>  
    <Child>2</Child>  
    <Child>3</Child>  
    <AnotherChild>4</AnotherChild>  
    <AnotherChild>5</AnotherChild>  
    <AnotherChild>6</AnotherChild>  
</Root>");  
XNamespace aw = "http://www.adventure-works.com";  
IEnumerable<XElement> c1 =  
    from el in root.Elements(aw + "Child")  
    select el;  
Console.WriteLine("Result set follows:");  
foreach (XElement el in c1)  
    Console.WriteLine((int)el);  
Console.WriteLine("End of result set");  
```  
  
 This example produces the following result:  
  
```  
Result set follows:  
1  
2  
3  
End of result set  
```  
  
## See Also  
 [Basic Queries (LINQ to XML) (C#)](../Topic/Basic%20Queries%20\(LINQ%20to%20XML\)%20\(C%23\).md)