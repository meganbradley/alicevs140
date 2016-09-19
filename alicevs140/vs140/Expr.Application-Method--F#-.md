---
title: "Expr.Application Method (F#)"
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
  - FSharpExpr.Application
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 82dfc5dd-0d8f-4f1d-892f-391e8ebfda45
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.Application Method (F#)
Creates an expression that represents the application of a first class function value to a single argument.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Application : Expr * Expr -> Expr  
  
// Usage:  
Expr.Application (functionExpr, argument)  
```  
  
#### Parameters  
 `functionExpr`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The function to apply.  
  
 `argument`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The argument to the function.  
  
## Return Value  
 The resulting expression.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Expr Class (F#)](../Topic/Quotations.Expr%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)