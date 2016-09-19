---
title: "Patterns.ForIntegerRangeLoop Active Pattern (F#)"
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
  - Patterns.( |ForIntegerRangeLoop|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: bf775c49-6b5b-4a45-97bf-9caa678e743f
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.ForIntegerRangeLoop Active Pattern (F#)
Recognizes expressions that represent looping operations over integer ranges.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |ForIntegerRangeLoop|_| ) : (input:Expr) -> (Var * Expr * Expr * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Var * Expr * Expr * Expr) option`. The option indicates whether there is a match to this pattern. In a pattern matching expression, the input is decomposed into a tuple of four elements upon a successful match. The first element represents the loop variable as a [Var](../vs140/Quotations.Var-Class--F#-.md) object, the second and third elements represent the beginning and ending of the range, and the last element represents the body of the loop.  
  
## Remarks  
 This function is named `ForIntegerRangeLoopPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)