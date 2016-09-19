---
title: "Serializing to an XmlReader (Invoking XSLT) (Visual Basic)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8b64f95a-e8f6-40f7-99f9-a8002c63af96
caps.latest.revision: 3
---
# Serializing to an XmlReader (Invoking XSLT) (Visual Basic)
When you use the <xref:System.Xml?qualifyHint=True> interoperability capabilities of [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)], you can use <xref:System.Xml.Linq.XNode.CreateReader?qualifyHint=False> to create an <xref:System.Xml.XmlReader?qualifyHint=False>. The module that reads from this <xref:System.Xml.XmlReader?qualifyHint=False> reads the nodes from the XML tree and processes them accordingly.  
  
## Invoking an XSLT Transformation  
 One possible use for this method is when invoking an XSLT transformation. You can create an XML tree, create an <xref:System.Xml.XmlReader?qualifyHint=False> from the XML tree, create a new document, and then create an <xref:System.Xml.XmlWriter?qualifyHint=False> to write into the new document. Then, you can invoke the XSLT transformation, passing in <xref:System.Xml.XmlReader?qualifyHint=False> and <xref:System.Xml.XmlWriter?qualifyHint=False>. After the transformation successfully completes, the new XML tree is populated with the results of the transformation.  
  
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
 [Serializing XML Trees (Visual Basic)](../Topic/Serializing%20XML%20Trees%20\(Visual%20Basic\).md)