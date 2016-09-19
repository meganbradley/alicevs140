---
title: "Patterns.Lambda Active Pattern (F#)"
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
  - Patterns.( |Lambda|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5f584ead-897b-4108-8c0d-7ba6a53a9e38
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.Lambda Active Pattern (F#)
Recognizes expressions that represent first-class function values.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Lambda|_| ) : (input:Expr) -> (Var * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Var * Expr) option`. The option indicates whether the input results in a match. In a pattern matching expression, the input is decomposed, upon a successful match, into a tuple of two elements. The first element is a [Var](../vs140/Quotations.Var-Class--F#-.md) object that represents a single argument. The second object is an expression that represents the body of the lambda expression. Lambda expressions that have multiple arguments are decomposed one argument at a time. For example, a lambda expression that has two arguments is decomposed so that the `Var` element is the first argument, and the `Expr` element is a lambda expression that can be recursively decomposed so that the second-level `Var` element is the second argument and the second-level `Expr` element is the body.  
  
## Remarks  
 This function is named `LambdaPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)