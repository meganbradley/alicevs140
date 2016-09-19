---
title: "How to: Load XML from a File (C#)"
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
ms.assetid: 3ed38487-8028-4209-9872-c8dce0ed4dfe
caps.latest.revision: 5
---
# How to: Load XML from a File (C#)
This topic shows how to load XML from a URI by using the <xref:System.Xml.Linq.XElement.Load?qualifyHint=True> method.  
  
## Example  
 The following example shows how to load an XML document from a file. The following example loads books.xml and outputs the XML tree to the console.  
  
 This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../vs140/Sample-XML-File--Books--LINQ-to-XML-1.md).  
  
```c#  
XElement booksFromFile = XElement.Load(@"books.xml");  
Console.WriteLine(booksFromFile);  
```  
  
 This code produces the following output:  
  
```xml  
<Catalog>  
  <Book id="bk101">  
    <Author>Garghentini, Davide</Author>  
    <Title>XML Developer's Guide</Title>  
    <Genre>Computer</Genre>  
    <Price>44.95</Price>  
    <PublishDate>2000-10-01</PublishDate>  
    <Description>An in-depth look at creating applications   
      with XML.</Description>  
  </Book>  
  <Book id="bk102">  
    <Author>Garcia, Debra</Author>  
    <Title>Midnight Rain</Title>  
    <Genre>Fantasy</Genre>  
    <Price>5.95</Price>  
    <PublishDate>2000-12-16</PublishDate>  
    <Description>A former architect battles corporate zombies,   
      an evil sorceress, and her own childhood to become queen   
      of the world.</Description>  
  </Book>  
</Catalog>  
```  
  
## See Also  
 [Parsing XML (C#)](../vs140/Parsing-XML--C#-.md)