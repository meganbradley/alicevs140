---
title: "&#39;Exit Try&#39; can only appear inside a &#39;Try&#39; statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8651df3-a32f-478c-a6d8-aa0ef584155f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Exit Try&#39; can only appear inside a &#39;Try&#39; statement
`Exit Try` can only appear within a `Try` block statement. Either you have a redundant `Exit Try` statement, or your `Exit Try` statement appears outside the bounds of its corresponding `Try` block.  
  
 **Error ID:** BC30393  
  
### To correct this error  
  
1.  Locate and remove the unnecessary `Exit Try` statement.  
  
2.  Move the `Exit Try`statement to the appropriate place within your code.  
  
## See Also  
 [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Structured Exception Handling Overview for Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)