---
title: "Patterns.NewUnionCase Active Pattern (F#)"
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
  - Patterns.( |NewUnionCase|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d361ce71-14fe-4c66-b99b-04ef429727e1
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.NewUnionCase Active Pattern (F#)
Recognizes expressions that represent the construction of particular union case values.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |NewUnionCase|_| ) : (input:Expr} -> (UnionCaseInfo * Expr list) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(UnionCaseInfo * Expr list) option`. The option type indicates whether the input results a successful match. In a pattern matching expression, the input is decomposed (upon a successful match) into a tuple of two elements. The first element is a [UnionCaseInfo](../Topic/Reflection.UnionCaseInfo%20Class%20\(F%23\).md) object that represents the case of a discriminated union, and the second element is an expression list that represents the arguments.  
  
## Remarks  
 This function is named `NewUnionCasePattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)