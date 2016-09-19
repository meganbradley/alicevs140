---
title: "Patterns.TupleGet Active Pattern (F#)"
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
  - Patterns.( |TupleGet|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3a11f5bb-fa3f-40af-8a75-e886b82a7f62
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.TupleGet Active Pattern (F#)
Recognizes expressions that represent getting a tuple field.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |TupleGet|_| ) : (input:Expr) -> (Expr * int) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return value is `(Expr * int) option`. The option type indicates whether there is a successful match. In a pattern matching expression, the input is decomposed, upon a successful match, into a tuple of two elements. The first is an expression that represents the tuple and the second is an integer that represents the zero-based index.  
  
## Remarks  
 This function is named `TupleGetPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)