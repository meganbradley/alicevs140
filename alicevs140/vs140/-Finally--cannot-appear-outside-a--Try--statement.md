---
title: "&#39;Finally&#39; cannot appear outside a &#39;Try&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0314d8d2-18bc-4bbd-858c-0a18408b52fd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Finally&#39; cannot appear outside a &#39;Try&#39; statement
`Finally` is used to complete a `Try...Catch...Finally` block; hence it can only appear once at the end of the block. Either you have an unnecessary `Finally`, or your `Finally` statement appears outside the bounds of its corresponding `Try` block.  
  
 **Error ID:** BC30382  
  
### To correct this error  
  
1.  Locate and remove the unnecessary `Finally`statement.  
  
2.  Move the `Finally` statement to the appropriate location in your code.  
  
## See Also  
 [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Structured Exception Handling Overview for Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)