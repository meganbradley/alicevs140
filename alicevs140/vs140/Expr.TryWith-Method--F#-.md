---
title: "Expr.TryWith Method (F#)"
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
  - FSharpExpr.TryWith
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: bb6a4a9f-0a49-4fe5-b4fd-b2167bda74e1
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.TryWith Method (F#)
Creates an expression that represents a `try...with` construct for exception filtering and catching.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member TryWith : Expr * Var * Expr * Var * Expr -> Expr  
  
// Usage:  
Expr.TryWith (body, filterVar, filterBody, catchVar, catchBody)  
```  
  
#### Parameters  
 `body`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The body of the try expression.  
  
 `filterVar`  
 Type: [Var](../vs140/Quotations.Var-Class--F#-.md)  
  
 `filterBody`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 `catchVar`  
 Type: [Var](../vs140/Quotations.Var-Class--F#-.md)  
  
 The variable to bind to a caught exception.  
  
 `catchBody`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The expression evaluated when an exception is caught.  
  
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