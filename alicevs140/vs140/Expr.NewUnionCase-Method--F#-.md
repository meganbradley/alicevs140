---
title: "Expr.NewUnionCase Method (F#)"
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
  - FSharpExpr.NewUnionCase
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 481c3359-71cd-404d-a2be-53208ffb9d9f
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.NewUnionCase Method (F#)
Creates an expression that represents the creation of a union case value.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member NewUnionCase : UnionCaseInfo * Expr list -> Expr  
  
// Usage:  
Expr.NewUnionCase (unionCase, arguments)  
```  
  
#### Parameters  
 `unionCase`  
 Type: [UnionCaseInfo](../Topic/Reflection.UnionCaseInfo%20Class%20\(F%23\).md)  
  
 The description of the union case.  
  
 `arguments`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The list of arguments for the case.  
  
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