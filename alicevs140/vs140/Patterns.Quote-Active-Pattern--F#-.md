---
title: "Patterns.Quote Active Pattern (F#)"
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
  - Patterns.( |Quote|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d164c678-ab7d-4836-bdb7-511af5647109
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.Quote Active Pattern (F#)
Recognizes expressions that represent a nested quotation literal.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Quote|_| ) : (input:Expr) -> Expr option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal type of the return value is `Expr option`. The option type represents whether the input expression produces a match. In a pattern matching expression, the input is decomposed into the expression enclosed by a nested quotation literal.  
  
## Remarks  
 This function is named `QuotePattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)