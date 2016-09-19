---
title: "Compiler Error C2099"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 30e151ee-d458-4901-b0c0-d45054a913f5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2099
initializer is not a constant  
  
 This error is issued only by the C compiler and occurs only for non-automatic variables.  The compiler initializes non-automatic variables at the start of the program and the values they are initialized with must be constant.  
  
## Example  
 The following sample generates C2099.  
  
```  
// C2099.c  
int j;  
int *p;  
j = *p;   // C2099 *p is not a constant  
```  
  
## Example  
 C2099 can also occur because the compiler is not able to perform constant folding on an expression under **/fp:strict** because the floating point precision environment settings (see [_controlfp_s](../vs140/_controlfp_s.md) for more information) may differ from compile to run time.  
  
 When constant folding fails, the compiler invokes dynamic initialization, which is not allowed in C.  
  
 To resolve this error, compile the module as a .cpp file or simplify the expression.  
  
 For more information, see [/fp (Specify Floating-Point Behavior)](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md).  
  
 The following sample generates C2099.  
  
```  
// C2099_2.c  
// compile with: /fp:strict /c  
float X = 2.0 - 1.0;   // C2099  
float X2 = 1.0;   // OK  
```