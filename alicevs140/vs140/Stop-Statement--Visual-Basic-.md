---
title: "Stop Statement (Visual Basic)"
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
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Stop Statement (Visual Basic)
Suspends execution.  
  
## Syntax  
  
```  
Stop  
```  
  
## Remarks  
 You can place `Stop` statements anywhere in procedures to suspend execution. Using the `Stop` statement is similar to setting a breakpoint in the code.  
  
 The `Stop` statement suspends execution, but unlike `End`, it does not close any files or clear any variables, unless it is encountered in a compiled executable (.exe) file.  
  
> [!NOTE]
>  If the `Stop` statement is encountered in code that is running outside of the integrated development environment (IDE), the debugger is invoked. This is true regardless of whether the code was compiled in debug or retail mode.  
  
## Example  
 This example uses the `Stop` statement to suspend execution for each iteration through the `For...Next` loop.  
  
 [!CODE [VbVbalrStatements#56](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#56)]  
  
## See Also  
 [End Statement](../vs140/End-Statement.md)