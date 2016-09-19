---
title: "&#39;End Try&#39; must be preceded by a matching &#39;Try&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d13357a-ab44-4082-b204-6e2e94f4774e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;End Try&#39; must be preceded by a matching &#39;Try&#39;
`End` `Try` is used to complete a `Try` block, and hence it can only appear at the end of the block. Either you have a redundant `End Try` statement, or your `End``Try` statement appears outside the bounds of its corresponding `Try` block.  
  
 **Error ID:** BC30383  
  
### To correct this error  
  
1.  Locate and remove the unnecessary `End Try`.  
  
2.  Move the `End Try` to the appropriate location in your code.  
  
## See Also  
 [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Structured Exception Handling Overview for Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)