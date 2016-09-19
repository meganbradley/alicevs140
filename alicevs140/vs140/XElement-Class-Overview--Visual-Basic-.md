---
title: "XElement Class Overview (Visual Basic)"
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
ms.assetid: 52331fcd-6023-4d19-b423-7b24f2d86ded
caps.latest.revision: 5
---
# XElement Class Overview (Visual Basic)
The <xref:System.Xml.Linq.XElement?qualifyHint=False> class is one of the fundamental classes in [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)]. It represents an XML element. You can use this class to create elements; change the content of the element; add, change, or delete child elements; add attributes to an element; or serialize the contents of an element in text form. You can also interoperate with other classes in <xref:System.Xml?qualifyHint=True>, such as <xref:System.Xml.XmlReader?qualifyHint=False>, <xref:System.Xml.XmlWriter?qualifyHint=False>, and <xref:System.Xml.Xsl.XslCompiledTransform?qualifyHint=False>.  
  
## XElement Functionality  
 This topic describes the functionality provided by the <xref:System.Xml.Linq.XElement?qualifyHint=False> class.  
  
### Constructing XML Trees  
 You can construct XML trees in a variety of ways, including the following:  
  
-   You can construct an XML tree in code. For more information, see [Creating XML Trees (Visual Basic)](../Topic/Creating%20XML%20Trees%20\(Visual%20Basic\).md).  
  
-   You can parse XML from various sources, including a <xref:System.IO.TextReader?qualifyHint=False>, text files, or a Web address (URL). For more information, see [Parsing XML (Visual Basic)](../Topic/Parsing%20XML%20\(Visual%20Basic\).md).  
  
-   You can use an <xref:System.Xml.XmlReader?qualifyHint=False> to populate the tree. For more information, see <xref:System.Xml.Linq.XNode.ReadFrom?qualifyHint=False>.  
  
-   If you have a module that can write content to an <xref:System.Xml.XmlWriter?qualifyHint=False>, you can use the <xref:System.Xml.Linq.XContainer.CreateWriter?qualifyHint=False> method to create a writer, pass the writer to the module, and then use the content that is written to the <xref:System.Xml.XmlWriter?qualifyHint=False> to populate the XML tree.  
  
 However, the most common way to create an XML tree is as follows:  
  
```vb  
Dim contacts As XElement = _  
    <Contacts>  
        <Contact>  
            <Name>Patrick Hines</Name>  
            <Phone>206-555-0144</Phone>  
            <Address>  
                <Street1>123 Main St</Street1>  
                <City>Mercer Island</City>  
                <State>WA</State>  
                <Postal>68042</Postal>  
            </Address>  
        </Contact>  
    </Contacts>  
```  
  
 Another very common technique for creating an XML tree involves using the results of a [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] query to populate an XML tree, as shown in the following example:  
  
```vb  
Dim srcTree As XElement = _  
    <Root>  
        <Element>1</Element>  
        <Element>2</Element>  
        <Element>3</Element>  
        <Element>4</Element>  
        <Element>5</Element>  
    </Root>  
Dim xmlTree As XElement = _  
    <Root>  
        <Child>1</Child>  
        <Child>2</Child>  
        <%= From el In srcTree.Elements() _  
            Where el.Value > 2 _  
            Select el %>  
    </Root>  
Console.WriteLine(xmlTree)  
```  
  
 This example produces the following output:  
  
```xml  
<Root>  
  <Child>1</Child>  
  <Child>2</Child>  
  <Element>3</Element>  
  <Element>4</Element>  
  <Element>5</Element>  
</Root>  
```  
  
### Serializing XML Trees  
 You can serialize the XML tree to a <xref:System.IO.File?qualifyHint=False>, a <xref:System.IO.TextWriter?qualifyHint=False>, or an <xref:System.Xml.XmlWriter?qualifyHint=False>.  
  
 For more information, see [Serializing XML Trees (Visual Basic)](../Topic/Serializing%20XML%20Trees%20\(Visual%20Basic\).md).  
  
### Retrieving XML Data via Axis Methods  
 You can use axis methods to retrieve attributes, child elements, descendant elements, and ancestor elements. [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries operate on axis methods, and provide several flexible and powerful ways to navigate through and process an XML tree.  
  
 For more information, see [LINQ to XML Axes (Visual Basic)](../Topic/LINQ%20to%20XML%20Axes%20\(Visual%20Basic\).md).  
  
### Querying XML Trees  
 You can write [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries that extract data from an XML tree.  
  
 For more information, see [Querying XML Trees (Visual Basic)](../vs140/Querying-XML-Trees--Visual-Basic-.md).  
  
### Modifying XML Trees  
 You can modify an element in a variety of ways, including changing its content or attributes. You can also remove an element from its parent.  
  
 For more information, see [Modifying XML Trees (LINQ to XML) (Visual Basic)](../Topic/Modifying%20XML%20Trees%20\(LINQ%20to%20XML\)%20\(Visual%20Basic\).md).  
  
## See Also  
 [LINQ to XML Programming Overview (Visual Basic)](../vs140/LINQ-to-XML-Programming-Overview--Visual-Basic-.md)