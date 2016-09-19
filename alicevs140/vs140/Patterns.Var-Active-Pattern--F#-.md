---
title: "Patterns.Var Active Pattern (F#)"
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
  - Patterns.( |Var|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fd28da2c-0ba3-4db2-85bc-73f7c23114e2
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.Var Active Pattern (F#)
Recognizes expressions that represent a variable.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Var|_| ) : (input:Expr) -> Var option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `Var option`. The option indicates whether the input results in a match. In a pattern matching expression, the input is represented as a [Var](../vs140/Quotations.Var-Class--F#-.md) object that represents a local value or variable.  
  
## Remarks  
 This function is named `VarPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)