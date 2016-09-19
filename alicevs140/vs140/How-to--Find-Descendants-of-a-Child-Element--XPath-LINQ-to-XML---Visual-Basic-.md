---
title: "How to: Find Descendants of a Child Element (XPath-LINQ to XML) (Visual Basic)"
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
ms.assetid: a958af40-f754-4409-85f9-7746978d4cb3
caps.latest.revision: 5
---
# How to: Find Descendants of a Child Element (XPath-LINQ to XML) (Visual Basic)
This topic shows how to get the descendant elements of a child element with a particular name.  
  
 The XPath expression is:  
  
 `./Paragraph//Text/text()`  
  
## Example  
 This example simulates the problems of extracting text from an XML representation of a word processing document. It first selects all `Paragraph` elements, and then it selects all `Text` descendant elements of each `Paragraph` element. This doesn't select the descendant `Text` elements of the `Comment` element.  
  
```vb  
Dim root As XElement = _  
    <Root>  
        <Paragraph>  
            <Text>This is the start of</Text>  
        </Paragraph>  
        <Comment>  
            <Text>This comment is not part of the paragraph text.</Text>  
        </Comment>  
        <Paragraph>  
            <Annotation Emphasis='true'>  
                <Text> a sentence.</Text>  
            </Annotation>  
        </Paragraph>  
        <Paragraph>  
            <Text>  This is a second sentence.</Text>  
        </Paragraph>  
    </Root>  
  
' LINQ to XML query  
Dim str1 As String = _  
    root.<Paragraph>...<Text>.Select(Function(ByVal s) s.Value). _  
    Aggregate( _  
        New StringBuilder(), _  
        Function(ByVal s, ByVal i) s.Append(i), _  
        Function(ByVal s) s.ToString())  
  
' XPath expression  
Dim str2 As String = DirectCast(root.XPathEvaluate("./Paragraph//Text/text()"), IEnumerable) _  
    .Cast(Of XText)().Select(Function(ByVal s) s.Value) _  
    .Aggregate( _  
        New StringBuilder(), _  
        Function(ByVal s, ByVal i) s.Append(i), _  
        Function(ByVal s) s.ToString())  
  
If str1 = str2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(str2)  
  
```  
  
 This example produces the following output:  
  
```  
Results are identical  
This is the start of a sentence.  This is a second sentence.  
```  
  
## See Also  
 [LINQ to XML for XPath Users (Visual Basic)](../Topic/LINQ%20to%20XML%20for%20XPath%20Users%20\(Visual%20Basic\).md)