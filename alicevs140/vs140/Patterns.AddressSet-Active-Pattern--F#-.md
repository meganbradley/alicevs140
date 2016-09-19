---
title: "Patterns.AddressSet Active Pattern (F#)"
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
  - Patterns.( |AddressSet|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 08abb9b7-ca3c-4170-886a-ee393e6aa5f7
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.AddressSet Active Pattern (F#)
Recognizes expressions that represent setting the value held at an address.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |AddressSet|_| ) : (input:Expr) -> (Expr * Expr) option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `(Expr * Expr) option`. The option is used to indicate whether there is a match to the pattern. In a pattern matching expression, the input expression is decomposed into a tuple of expressions. The first expression represents the left side of an assignment to a mutable variable that is local to a function, and the second expression represents the right side of the assignment.  
  
## Remarks  
 This function is named `AddressSetPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)