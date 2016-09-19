---
title: "How to: Create a Tree from an XmlReader (Visual Basic)"
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
ms.assetid: 6de683d8-177d-402b-b0de-d0539f1ce5d8
caps.latest.revision: 3
---
# How to: Create a Tree from an XmlReader (Visual Basic)
This topic shows how to create an XML tree directly from an <xref:System.Xml.XmlReader?qualifyHint=False>. To create an <xref:System.Xml.Linq.XElement?qualifyHint=False> from an <xref:System.Xml.XmlReader?qualifyHint=False>, you must position the <xref:System.Xml.XmlReader?qualifyHint=False> on an element node. The <xref:System.Xml.XmlReader?qualifyHint=False> will skip comments and processing instructions, but if the <xref:System.Xml.XmlReader?qualifyHint=False> is positioned on a text node, an error will be thrown. To avoid such errors, always position the <xref:System.Xml.XmlReader?qualifyHint=False> on an element before you create an XML tree from the <xref:System.Xml.XmlReader?qualifyHint=False>.  
  
## Example  
 This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../vs140/Sample-XML-File--Books--LINQ-to-XML-3.md).  
  
 The following code creates an `T:System.Xml.XmlReader` object, and then reads nodes until it finds the first element node. It then loads the <xref:System.Xml.Linq.XElement?qualifyHint=False> object.  
  
```vb  
Dim r As XmlReader = XmlReader.Create("books.xml")  
Do While r.NodeType <> XmlNodeType.Element  
    r.Read()  
Loop  
Dim e As XElement = XElement.Load(r)  
Console.WriteLine(e)  
```  
  
 This example produces the following output:  
  
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