---
title: "&lt;see&gt; (Visual Basic)"
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
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;see&gt; (Visual Basic)
Specifies a link to another member.  
  
## Syntax  
  
```  
<see cref="member"/>  
```  
  
#### Parameters  
 `member`  
 A reference to a member or field that is available to be called from the current compilation environment. The compiler checks that the given code element exists and passes `member` to the element name in the output XML. `member` must appear within double quotation marks (" ").  
  
## Remarks  
 Use the `<see>` tag to specify a link from within text. Use [<seealso\> (Visual Basic)](../vs140/-seealso---Visual-Basic-.md) to indicate text that you might want to appear in a "See Also" section.  
  
 Compile with [/doc](../vs140/-doc.md) to process documentation comments to a file.  
  
## Example  
 This example uses the `<see>` tag in the `UpdateRecord` remarks section to refer to the `DoesRecordExist` method.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## See Also  
 [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)