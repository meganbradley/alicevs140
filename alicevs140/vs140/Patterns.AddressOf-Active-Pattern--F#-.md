---
title: "Patterns.AddressOf Active Pattern (F#)"
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
  - Patterns.( |AddressOf|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: dc14214e-96a1-43b7-ae8c-44d2b78dad4d
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Patterns.AddressOf Active Pattern (F#)
Recognizes expressions that represent getting the address of a value.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.Patterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |AddressOf|_| ) : (input:Expr) -> Expr option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The formal return type is `Expr option`. The option indicates whether there is a match to this pattern. In the context of a pattern matching expression, the result of this pattern is an expression whose address is taken.  
  
## Remarks  
 This function is named `AddressOfPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Patterns Module (F#)](../vs140/Quotations.Patterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)