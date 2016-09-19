---
title: "How to: Populate an XML Tree with an XmlWriter (LINQ to XML) (Visual Basic)"
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
ms.assetid: 5792a0eb-94ee-440d-b601-58cca8c0ee0b
caps.latest.revision: 5
---
# How to: Populate an XML Tree with an XmlWriter (LINQ to XML) (Visual Basic)
One way to populate an XML tree is to use <xref:System.Xml.Linq.XContainer.CreateWriter?qualifyHint=False> to create an <xref:System.Xml.XmlWriter?qualifyHint=False>, and then write to the <xref:System.Xml.XmlWriter?qualifyHint=False>. The XML tree is populated with all nodes that are written to the <xref:System.Xml.XmlWriter?qualifyHint=False>.  
  
 You would typically use this method when you use [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] with another class that expects to write to an <xref:System.Xml.XmlWriter?qualifyHint=False>, such as <xref:System.Xml.Xsl.XslCompiledTransform?qualifyHint=False>.  
  
## Example  
 One possible use for <xref:System.Xml.Linq.XContainer.CreateWriter?qualifyHint=False> is when invoking an XSLT transformation. This example creates an XML tree, creates an <xref:System.Xml.XmlReader?qualifyHint=False> from the XML tree, creates a new document, and then creates an <xref:System.Xml.XmlWriter?qualifyHint=False> to write into the new document. It then invokes the XSLT transformation, passing in <xref:System.Xml.XmlReader?qualifyHint=False> and <xref:System.Xml.XmlWriter?qualifyHint=False>. After the transformation successfully completes, the new XML tree is populated with the results of the transformation.  
  
```vb  
Dim xslMarkup As XDocument = _  
    <?xml version='1.0'?>   
    <xsl:stylesheet xmlns:xsl='http://www.w3.org/1999/XSL/Transform' version='1.0'>  
        <xsl:template match='/Parent'>  
            <Root>  
                <C1>  
                    <xsl:value-of select='Child1'/>  
                </C1>  
                <C2>  
                    <xsl:value-of select='Child2'/>  
                </C2>  
            </Root>  
        </xsl:template>  
    </xsl:stylesheet>  
  
Dim xmlTree As XDocument = _  
    <?xml version='1.0'?>  
    <Parent>  
        <Child1>Child1 data</Child1>  
        <Child2>Child2 data</Child2>  
    </Parent>  
  
Dim newTree As XDocument = New XDocument()  
Using writer As XmlWriter = newTree.CreateWriter()  
    ' Load the style sheet.  
    Dim xslt As XslCompiledTransform = New XslCompiledTransform()  
    xslt.Load(xslMarkup.CreateReader())  
  
    ' Execute the transformation and output the results to a writer.  
    xslt.Transform(xmlTree.CreateReader(), writer)  
End Using  
  
Console.WriteLine(newTree)  
```  
  
 This example produces the following output:  
  
```xml  
<Root>  
  <C1>Child1 data</C1>  
  <C2>Child2 data</C2>  
</Root>  
```  
  
## See Also  
 <xref:System.Xml.Linq.XContainer.CreateWriter?qualifyHint=False>   
 <xref:System.Xml.XmlWriter?qualifyHint=False>   
 <xref:System.Xml.Xsl.XslCompiledTransform?qualifyHint=False>   
 [Creating XML Trees (Visual Basic)](../Topic/Creating%20XML%20Trees%20\(Visual%20Basic\).md)