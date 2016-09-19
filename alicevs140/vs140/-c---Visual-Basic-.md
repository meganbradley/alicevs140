---
title: "&lt;c&gt; (Visual Basic)"
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
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;c&gt; (Visual Basic)
Indicates that text within a description is code.  
  
## Syntax  
  
```  
<c>text</c>  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`text`|The text you would like to indicate as code.|  
  
## Remarks  
 The `<c>` tag gives you a way to indicate that text within a description should be marked as code. Use [<code\> (Visual Basic)](../vs140/-code---Visual-Basic-.md) to indicate multiple lines as code.  
  
 Compile with [/doc](../vs140/-doc.md) to process documentation comments to a file.  
  
## Example  
 This example uses the `<c>` tag in the summary section to indicate that `Counter` is code.  
  
 [!CODE [VbVbcnXmlDocComments#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#1)]  
  
## See Also  
 [Recommended Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)