---
title: "Loop Structures (Visual Basic)"
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
ms.assetid: ecacb09b-a4c9-42be-98b2-a15d368b5db8
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Loop Structures (Visual Basic)
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] loop structures allow you to run one or more lines of code repetitively. You can repeat the statements in a loop structure until a condition is `True`, until a condition is `False`, a specified number of times, or once for each element in a collection.  
  
 The following illustration shows a loop structure that runs a set of statements until a condition becomes true.  
  
 ![Flow chart of a Do...Until loop](../vs140/media/DoUntilLoop.gif "DoUntilLoop")  
Running a set of statements until a condition becomes true  
  
## While Loops  
 The `While`...`End While` construction runs a set of statements as long as the condition specified in the `While` statement is `True`. For more information, see [While...End While Statement (Visual Basic)](../Topic/While...End%20While%20Statement%20\(Visual%20Basic\).md).  
  
## Do Loops  
 The `Do`...`Loop` construction allows you to test a condition at either the beginning or the end of a loop structure. You can also specify whether to repeat the loop while the condition remains `True` or until it becomes `True`. For more information, see [Do...Loop Statement (Visual Basic)](../vs140/Do...Loop-Statement--Visual-Basic-.md).  
  
## For Loops  
 The `For`...`Next` construction performs the loop a set number of times. It uses a loop control variable, also called a *counter*, to keep track of the repetitions. You specify the starting and ending values for this counter, and you can optionally specify the amount by which it increases from one repetition to the next. For more information, see [For...Next Statement (Visual Basic)](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md).  
  
## For Each Loops  
 The `For Each`...`Next` construction runs a set of statements once for each element in a collection. You specify the loop control variable, but you do not have to determine starting or ending values for it. For more information, see [For Each...Next Statement (Visual Basic)](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md).  
  
## See Also  
 [Control Flow in Visual Basic](../vs140/Control-Flow-in-Visual-Basic.md)   
 [Decision Structures](../vs140/Decision-Structures--Visual-Basic-.md)   
 [Other Control Structures](../vs140/Other-Control-Structures--Visual-Basic-.md)   
 [Nested Control Structures](../vs140/Nested-Control-Structures--Visual-Basic-.md)