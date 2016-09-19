---
title: "Expr.UnionCaseTest Method (F#)"
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
  - FSharpExpr.UnionCaseTest
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a9d0803c-863c-493b-81ac-964a6b4f230a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.UnionCaseTest Method (F#)
Creates an expression that represents a test of a value is of a particular union case.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member UnionCaseTest : Expr * UnionCaseInfo -> Expr  
  
// Usage:  
Expr.UnionCaseTest (source, unionCase)  
```  
  
#### Parameters  
 `source`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The expression to test.  
  
 `unionCase`  
 Type: [UnionCaseInfo](../Topic/Reflection.UnionCaseInfo%20Class%20\(F%23\).md)  
  
 The description of the union case.  
  
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