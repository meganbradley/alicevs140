---
title: "Branching out of a &#39;Finally&#39; is not valid"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 16a0dc29-3657-4373-b77f-38f3cb80e6c9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Branching out of a &#39;Finally&#39; is not valid
A `GoTo` statement inside a `Finally` block branches outside the block. It is not valid to branch into or out of a `Catch` or `Finally` block.  
  
 **Error ID:** BC30101  
  
### To correct this error  
  
-   Remove the `GoTo` statement, and consider implementing the program logic with decision or loop control structures.  
  
## See Also  
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [GoTo Statement](../vs140/GoTo-Statement.md)   
 [Control Flow](../vs140/Control-Flow-in-Visual-Basic.md)