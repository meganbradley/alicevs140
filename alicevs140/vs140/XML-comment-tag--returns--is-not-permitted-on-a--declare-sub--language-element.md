---
title: "XML comment tag &#39;returns&#39; is not permitted on a &#39;declare sub&#39; language element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55ba3e8a-ba7f-42e3-a4a7-b22844e72564
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML comment tag &#39;returns&#39; is not permitted on a &#39;declare sub&#39; language element
XML comment tag 'returns' is not permitted on a 'declare sub' language element. XML comment will be ignored.  
  
 An XML comment for a `Declare Sub` declaration cannot contain a `<`returns`>` tag.  
  
 **Error ID:** BC42315  
  
### To correct this error  
  
-   Remove the unsupported `<`returns`>` tag.  
  
## See Also  
 [<returns\> (Visual Basic)](../vs140/-returns---Visual-Basic-.md)   
 [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)   
 [Documenting Your Code with XML (Visual Basic)](../vs140/Documenting-Your-Code-with-XML--Visual-Basic-.md)   
 [Declare Statement](../Topic/Declare%20Statement.md)