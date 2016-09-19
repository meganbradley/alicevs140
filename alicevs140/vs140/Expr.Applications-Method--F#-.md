---
title: "Expr.Applications Method (F#)"
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
  - FSharpExpr.Applications
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7abf4dd2-e607-4341-8a63-d59b5adc9228
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.Applications Method (F#)
Creates an expression that represents the application of a first class function value to multiple arguments.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Applications : Expr * Expr list list -> Expr  
  
// Usage:  
Expr.Applications (functionExpr, arguments)  
```  
  
#### Parameters  
 `functionExpr`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The function to apply.  
  
 `arguments`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)[list](../vs140/Collections.List--T--Union--F#-.md)[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The list of lists of arguments to the function.  
  
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