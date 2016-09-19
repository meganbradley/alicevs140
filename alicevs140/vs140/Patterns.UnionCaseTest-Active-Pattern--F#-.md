---
title: "Patterns.UnionCaseTest Active Pattern (F#)"
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
  - Patterns.( |UnionCaseTest|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fb65b0a3-68d0-4223-be01-fe68ff2a8d57
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.UnionCaseTest Active Pattern (F#)
Recognizes expressions that represent an operation that tests whether a value is of a particular union case.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |UnionCaseTest|_| ) : (input:Expr) -> (Expr * UnionCaseInfo) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr * UnionCaseInfo) option`. The option indicates whether the input results in a match. In a pattern matching expression, the input is decomposed into a tuple of two elements. The first element is the expression that represents the target of the test and the second element is the [UnionCaseInfo](../Topic/Reflection.UnionCaseInfo%20Class%20\(F%23\).md) object that represents the union case.  
  
## Remarks  
 This function is named `UnionCaseTestPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)