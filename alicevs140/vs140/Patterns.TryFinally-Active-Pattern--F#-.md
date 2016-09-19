---
title: "Patterns.TryFinally Active Pattern (F#)"
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
  - Patterns.( |TryFinally|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 30d985b7-3989-4baf-89e5-2b88dcafe648
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.TryFinally Active Pattern (F#)
Recognizes expressions that represent a `try...finally` construct.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |TryFinally|_| ) : (input:Expr) -> (Expr * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr * Expr) option`. The option type indicates whether the input expression results in a match. In a pattern matching expression, the input expression is decomposed, upon a successful match, into a tuple of two expressions. The first expression represents the code in the `try` block. The second expression represents the code in the `finally` block.  
  
## Remarks  
 This function is named `TryFinallyPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)