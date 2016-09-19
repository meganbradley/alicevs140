---
title: "VERIFY"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e1ab4ee-cbc7-4290-a777-c92f42ce7b96
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VERIFY
In the Debug version of MFC, evaluates its argument.  
  
## Syntax  
  
```  
  
VERIFY(  
booleanExpression )  
```  
  
#### Parameters  
 `booleanExpression`  
 Specifies an expression (including pointer values) that evaluates to nonzero or 0.  
  
## Remarks  
 If the result is 0, the macro prints a diagnostic message and halts the program. If the condition is nonzero, it does nothing.  
  
 The diagnostic message has the form  
  
 `assertion failed in file <name> in line <num>`  
  
 where *name* is the name of the source file and *num* is the line number of the assertion that failed in the source file.  
  
 In the Release version of MFC, **VERIFY** evaluates the expression but does not print or interrupt the program. For example, if the expression is a function call, the call will be made.  
  
## Example  
 [!CODE [NVC_MFCDocView#198](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#198)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ASSERT](../vs140/ASSERT--MFC-.md)