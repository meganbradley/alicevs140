---
title: "&lt;exception&gt; (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c0517549-171e-4dae-ab88-a9c1700b6eee
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;exception&gt; (Visual Basic)
Specifies which exceptions can be thrown.  
  
## Syntax  
  
```  
<exception cref="member">description</exception>  
```  
  
#### Parameters  
 `member`  
 A reference to an exception that is available from the current compilation environment. The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML. `member` must appear within double quotation marks (" ").  
  
 `description`  
 A description.  
  
## Remarks  
 Use the `<exception>` tag to specify which exceptions can be thrown. This tag is applied to a method definition.  
  
 Compile with [/doc](../vs140/-doc.md) to process documentation comments to a file.  
  
## Example  
 This example uses the `<exception>` tag to describe an exception that the `IntDivide` function can throw.  
  
 [!CODE [VbVbcnXmlDocComments#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#3)]  
  
## See Also  
 [Recommended Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)