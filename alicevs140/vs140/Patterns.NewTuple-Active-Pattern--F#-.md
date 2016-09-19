---
title: "Patterns.NewTuple Active Pattern (F#)"
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
  - Patterns.( |NewTuple|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2808be50-9b00-47e8-bbde-caf7180b6bbb
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.NewTuple Active Pattern (F#)
Recognizes expressions that represent the construction of tuple values.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |NewTuple|_| ) : (input:Expr) -> (Expr list) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr list) option`. The option indicates whether the input results in a match. In a pattern matching expression, the input is decomposed into a list of expressions that form the tuple definition.  
  
## Remarks  
 This function is named `NewTuplePattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)