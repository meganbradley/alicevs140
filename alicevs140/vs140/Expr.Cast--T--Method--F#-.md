---
title: "Expr.Cast&lt;&#39;T&gt; Method (F#)"
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
  - FSharpExpr.Cast<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ec6eeb85-8790-45d1-9846-0433cbd360bd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.Cast&lt;&#39;T&gt; Method (F#)
Returns a new typed expression given an underlying runtime-typed expression. A type annotation is usually required to use this function, and using an incorrect type annotation may result in a later runtime exception.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Cast : Expr -> Expr<'T>  
  
// Usage:  
Expr.Cast (source)  
```  
  
#### Parameters  
 `source`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The expression to cast.  
  
## Return Value  
 The resulting typed expression.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Expr Class (F#)](../Topic/Quotations.Expr%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)