---
title: "XML documentation parse error: Start tag &#39;&lt;tag&gt;&#39; doesn&#39;t have a matching end tag"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 45b68176-ebf6-43af-820e-6801aabb6c57
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML documentation parse error: Start tag &#39;&lt;tag&gt;&#39; doesn&#39;t have a matching end tag
XML documentation parse error: Start tag <tag\> doesn't have a matching end tag. XML comment will be ignored.  
  
 The XML comment contains a start tag but does not contain a matching end tag.  
  
 **Error ID:** BC42316  
  
### To correct this error  
  
-   Add an end tag that matches the start tag.  
  
     — or —  
  
-   If the tag contains no inner text, such as [<seealso\> (Visual Basic)](../vs140/-seealso---Visual-Basic-.md), specify a forward slash before the closing angle bracket.  
  
## See Also  
 [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)   
 [Documenting Your Code with XML (Visual Basic)](../vs140/Documenting-Your-Code-with-XML--Visual-Basic-.md)