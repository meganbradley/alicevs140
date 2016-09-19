---
title: "Patterns.Application Active Pattern (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
apiname: 
  - Patterns.( |Application|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 57856b28-771f-4ceb-9f00-16ea7f48af46
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.Application Active Pattern (F#)
Recognizes expressions that represent applications of first-class function values.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Application|_| ) : (input:Expr) -> (Expr * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr * Expr) option`. The option indicates whether a match exists. When you use the active pattern in a match expression, you use the tuple of two expressions directly to decompose the pattern.  
  
 The tuple contains two expressions that result from the decomposition of a curried function application expression. If there is one curried argument, the first expression represents the function name and the second expression represents the argument. If there are multiple curried arguments, the first expression is itself a function application that contains all the curried arguments except the last, and the second expression represents the last curried argument. The first expression can be recursively processed to decompose the next curried argument of the function.  
  
## Remarks  
 This function is named `ApplicationPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)