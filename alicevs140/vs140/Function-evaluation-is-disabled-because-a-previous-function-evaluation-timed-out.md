---
title: "Function evaluation is disabled because a previous function evaluation timed out"
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
ms.assetid: 561e593a-f50a-4b72-a708-4cab60ec7b28
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Function evaluation is disabled because a previous function evaluation timed out
Function evaluation is disabled because a previous function evaluation timed out. To re-enable function evaluation, step again or restart debugging.  
  
 In the Visual Studio debugger, an expression specifies a procedure call, but another evaluation has timed out.  
  
 Possible causes for a procedure call to time out include an infinite loop or *endless loop*. For more information, see [For...Next Statement (Visual Basic)](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md).  
  
 A special case of an infinite loop is *recursion*. For more information, see [Recursive Procedures](../Topic/Recursive%20Procedures%20\(Visual%20Basic\).md).  
  
 **Error ID:** BC30957  
  
### To correct this error  
  
1.  If possible, determine what the previous function evaluation was and what caused it to time out. Otherwise, you might encounter this error again.  
  
2.  Either step the debugger again, or terminate and restart debugging.  
  
## See Also  
 [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md)   
 [Start, Break, Step, Run through Code, and Stop Debugging in Visual Studio](../vs140/Navigating-through-Code-with-the-Debugger.md)   
 [Expressions in Visual Basic](../vs140/Expressions-in-Visual-Basic.md)