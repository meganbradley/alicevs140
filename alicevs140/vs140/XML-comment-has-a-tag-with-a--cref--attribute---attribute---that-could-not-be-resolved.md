---
title: "XML comment has a tag with a &#39;cref&#39; attribute &#39;&lt;attribute&gt;&#39; that could not be resolved"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c9f3cfa5-565f-48bf-8616-cfb25d24f89e
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML comment has a tag with a &#39;cref&#39; attribute &#39;&lt;attribute&gt;&#39; that could not be resolved
XML comment has a tag with a 'cref' attribute <attribute\> that could not be resolved. XML comment will be ignored.  
  
 Tags can have a `cref` attribute that designates a link to another element of the XML by specifying the relative name of the identifier. At compile time, the compiler replaces the value with the qualified XML identifier for the value pointed at by the user. The compiler uses its normal resolution rules for finding the type or member.  
  
 **Error ID:** BC42309  
  
### To correct this error  
  
-   Validate the `cref` attribute so that it points to a valid code element.  
  
## See Also  
 [How to: Create XML Documentation in Visual Basic](../vs140/How-to--Create-XML-Documentation-in-Visual-Basic.md)   
 [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)