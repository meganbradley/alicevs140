---
title: "XAttribute Class Overview (Visual Basic)"
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
ms.assetid: 7781580a-9583-4a1b-ae1e-91c5936eb0b1
caps.latest.revision: 5
---
# XAttribute Class Overview (Visual Basic)
Attributes are name/value pairs that are associated with an element. The <xref:System.Xml.Linq.XAttribute?qualifyHint=False> class represents XML attributes.  
  
## Overview  
 Working with attributes in [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] is similar to working with elements. Their constructors are similar. The methods that you use to retrieve collections of them are similar. A [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] query expression for a collection of attributes looks very similar to a [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] query expression for a collection of elements.  
  
 The order in which attributes were added to an element is preserved. That is, when you iterate through the attributes, you see them in the same order that they were added.  
  
## The XAttribute Constructor  
 The following constructor of the <xref:System.Xml.Linq.XAttribute?qualifyHint=False> class is the one that you will most commonly use:  
  
|Constructor|Description|  
|-----------------|-----------------|  
|`XAttribute(XName name, object content)`|Creates an <xref:System.Xml.Linq.XAttribute?qualifyHint=False> object. The `name` argument specifies the name of the attribute; `content` specifies the content of the attribute.|  
  
### Creating an Element with an Attribute  
 The following code shows an element that contains an attribute using XML literals in Visual Basic:  
  
```vb  
Dim phone As XElement = <Phone Type="Home">555-555-5555</Phone>  
Console.WriteLine(phone)  
```  
  
 This example produces the following output:  
  
```xml  
<Phone Type="Home">555-555-5555</Phone>  
```  
  
### Functional Construction of Attributes  
 You can construct <xref:System.Xml.Linq.XAttribute?qualifyHint=False> objects in-line with the construction of <xref:System.Xml.Linq.XElement?qualifyHint=False> objects, as follows:  
  
```vb  
Dim c As XElement = _  
    <Customers>  
        <Customer>  
            <Name>John Doe</Name>  
            <PhoneNumbers>  
                <Phone type="home">555-555-5555</Phone>  
                <Phone type="work">666-666-6666</Phone>  
            </PhoneNumbers>  
        </Customer>  
    </Customers>  
Console.WriteLine(c)  
```  
  
 This example produces the following output:  
  
```xml  
<Customers>  
  <Customer>  
    <Name>John Doe</Name>  
    <PhoneNumbers>  
      <Phone type="home">555-555-5555</Phone>  
      <Phone type="work">666-666-6666</Phone>  
    </PhoneNumbers>  
  </Customer>  
</Customers>  
```  
  
### Attributes Are Not Nodes  
 There are some differences between attributes and elements. <xref:System.Xml.Linq.XAttribute?qualifyHint=False> objects are not nodes in the XML tree. They are name/value pairs associated with an XML element. In contrast to the Document Object Model (DOM), this more closely reflects the structure of XML. Although <xref:System.Xml.Linq.XAttribute?qualifyHint=False> objects are not actually nodes in the XML tree, working with <xref:System.Xml.Linq.XAttribute?qualifyHint=False> objects is very similar to working with <xref:System.Xml.Linq.XElement?qualifyHint=False> objects.  
  
 This distinction is primarily important only to developers who are writing code that works with XML trees at the node level. Many developers will not be concerned with this distinction.  
  
## See Also  
 [LINQ to XML Programming Overview (Visual Basic)](../vs140/LINQ-to-XML-Programming-Overview--Visual-Basic-.md)