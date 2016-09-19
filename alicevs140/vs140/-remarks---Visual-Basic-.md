---
title: "&lt;remarks&gt; (Visual Basic)"
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
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;remarks&gt; (Visual Basic)
Specifies a remarks section for the member.  
  
## Syntax  
  
```  
<remarks>description</remarks>  
```  
  
#### Parameters  
 `description`  
 A description of the member.  
  
## Remarks  
 Use the `<remarks>` tag to add information about a type, supplementing the information specified with [<summary\> (Visual Basic)](../vs140/-summary---Visual-Basic-.md).  
  
 This information appears in the Object Browser. For information about the Object Browser, see [Viewing the Structure of Code](../vs140/Viewing-the-Structure-of-Code.md).  
  
 Compile with [/doc](../vs140/-doc.md) to process documentation comments to a file.  
  
## Example  
 This example uses the `<remarks>` tag to explain what the `UpdateRecord` method does.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## See Also  
 [Recommended Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)