---
title: "Using XSLT to Transform an XML Tree (Visual Basic)"
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
ms.assetid: 3390ca68-c270-4e1d-b64b-6a063a77017c
caps.latest.revision: 5
---
# Using XSLT to Transform an XML Tree (Visual Basic)
You can create an XML tree, create an <xref:System.Xml.XmlReader?qualifyHint=False> from the XML tree, create a new document, and create an <xref:System.Xml.XmlWriter?qualifyHint=False> that will write into the new document. Then, you can invoke the XSLT transformation, passing the <xref:System.Xml.XmlReader?qualifyHint=False> and <xref:System.Xml.XmlWriter?qualifyHint=False> to the transformation. After the transformation successfully completes, the new XML tree is populated with the results of the transform.  
  
## Example  
  
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
  
Dim xmlTree As XElement = _   
    <Parent>  
        <Child1>Child1 data</Child1>  
        <Child2>Child2 data</Child2>  
    </Parent>  
  
Dim newTree As XDocument = New XDocument()  
  
Using writer As XmlWriter = newTree.CreateWriter()  
    ' Load the style sheet.  
    Dim xslt As XslCompiledTransform = _  
        New XslCompiledTransform()  
    xslt.Load(xslMarkup.CreateReader())  
  
    ' Execute the transform and output the results to a writer.  
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
 <xref:System.Xml.Linq.XContainer.CreateWriter?qualifyHint=True>   
 <xref:System.Xml.Linq.XNode.CreateReader?qualifyHint=True>   
 [Advanced LINQ to XML Programming (Visual Basic)](../Topic/Advanced%20LINQ%20to%20XML%20Programming%20\(Visual%20Basic\).md)