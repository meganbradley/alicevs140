---
title: "How to: Find Descendants with a Specific Element Name (Visual Basic)"
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
ms.assetid: 78915518-0d25-4051-ab55-929779989510
caps.latest.revision: 5
---
# How to: Find Descendants with a Specific Element Name (Visual Basic)
Sometimes you want to find all descendants with a particular name. You could write code to iterate through all of the descendants, but it is easier to use the <xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=False> axis.  
  
## Example  
 The following example shows how to find descendants based on the element name.  
  
```vb  
Dim root As XElement = _  
    <root>  
        <para>  
            <r>  
                <t>Some text </t>  
            </r>  
            <n>  
                <r>  
                    <t>that is broken up into </t>  
                </r>  
            </n>  
            <n>  
                <r>  
                    <t>multiple segments.</t>  
                </r>  
            </n>  
        </para>  
    </root>  
  
Dim textSegs As IEnumerable(Of String) = _  
    From seg In root...<t> _  
    Select seg.Value  
  
Dim str As String = textSegs.Aggregate( _  
    New StringBuilder, _  
    Function(sb, i) sb.Append(i), _  
    Function(sb) sb.ToString)  
  
Console.WriteLine(str)  
```  
  
 This code produces the following output:  
  
```  
Some text that is broken up into multiple segments.  
```  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (Visual Basic)](../Topic/Working%20with%20XML%20Namespaces%20\(Visual%20Basic\).md).  
  
```vb  
Imports <xmlns='http://www.adatum.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = _  
            <root>  
                <para>  
                    <r>  
                        <t>Some text </t>  
                    </r>  
                    <n>  
                        <r>  
                            <t>that is broken up into </t>  
                        </r>  
                    </n>  
                    <n>  
                        <r>  
                            <t>multiple segments.</t>  
                        </r>  
                    </n>  
                </para>  
            </root>  
  
        Dim textSegs As IEnumerable(Of String) = _  
            From seg In root...<t> _  
            Select seg.Value  
  
        Dim str As String = textSegs.Aggregate( _  
            New StringBuilder, _  
            Function(sb, i) sb.Append(i), _  
            Function(sb) sb.ToString)  
  
        Console.WriteLine(str)  
    End Sub  
End Module  
```  
  
 This code produces the following output:  
  
```  
Some text that is broken up into multiple segments.  
```  
  
## See Also  
 <xref:System.Xml.Linq.XContainer.Descendants?qualifyHint=False>   
 [Basic Queries (LINQ to XML) (Visual Basic)](../vs140/Basic-Queries--LINQ-to-XML---Visual-Basic-.md)