---
title: "Patterns.IfThenElse Active Pattern (F#)"
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
  - Patterns.( |IfThenElse|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 90f83178-ad5e-4a9f-b657-50e955e2738b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.IfThenElse Active Pattern (F#)
Recognizes expressions that represent conditionals.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |IfThenElse|_| ) : (input:Expr) -> (Expr * Expr * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr * Expr * Expr) option`. The option determines whether there is a match. In a pattern matching expression, the input is decomposed upon a match into a tuple of three expressions. The first element is the test condition. The second element is the expression after the `then` keyword that is executed if the test condition is true. The third element is the expression after the `else` keyword.  
  
## Remarks  
 This function is named `IfThenElsePattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)