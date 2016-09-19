---
title: "How to: Load XML from a File (Visual Basic)"
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
ms.assetid: e2d337ad-8ac8-4671-b694-30e5ca1413b7
caps.latest.revision: 5
---
# How to: Load XML from a File (Visual Basic)
This topic shows how to load XML from a URI by using the <xref:System.Xml.Linq.XElement.Load?qualifyHint=True> method.  
  
## Example  
 The following example shows how to load an XML document from a file. The following example loads books.xml and outputs the XML tree to the console.  
  
 This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../vs140/Sample-XML-File--Books--LINQ-to-XML-3.md).  
  
```vb  
Dim booksFromFile As XElement = XElement.Load("books.xml")  
Console.WriteLine(booksFromFile)  
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
 [Parsing XML (Visual Basic)](../Topic/Parsing%20XML%20\(Visual%20Basic\).md)