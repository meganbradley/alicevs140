---
title: "DerivedPatterns.Applications Active Pattern (F#)"
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
  - DerivedPatterns.( |Applications|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b7b396fd-0242-4107-88e2-759fbae8ea75
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DerivedPatterns.Applications Active Pattern (F#)
Recognizes expressions that represent the application of a (possibly curried or tupled) first-class function value  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.DerivedPatterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Applications|_| ) : (input:Expr) -> (Expr * Expr list list) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return value is `(Expr * Expr list list) option`. The option indicates whether the input results in a match. In a pattern matching expression, the input is decomposed, upon a successful match, into a tuple of two elements. The first element is an expression that represents the function. The second element is a list of lists of expressions that represent the curried and tuple arguments of the function.  
  
## Remarks  
 This function is named `ApplicationsPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.DerivedPatterns Module (F#)](../vs140/Quotations.DerivedPatterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)