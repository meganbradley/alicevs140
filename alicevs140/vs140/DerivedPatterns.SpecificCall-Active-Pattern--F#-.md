---
title: "DerivedPatterns.SpecificCall Active Pattern (F#)"
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
  - DerivedPatterns.( |SpecificCall|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 05a77b21-20fe-4b9a-8e07-aa999538198d
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DerivedPatterns.SpecificCall Active Pattern (F#)
Recognizes calls to a specified function or method. This is a parameterized active pattern.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.DerivedPatterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |SpecificCall|_| ) : (templateParameter:Expr) -> Expr -> (Expr option * Type list * Expr list) option  
```  
  
#### Parameters  
 `templateParameter`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input template expression that specifies the method to call.  
  
## Return Value  
 The formal return type is `(Expr option * Type list * Expr list) option`. The option indicates whether there is a successful match. In a pattern matching expression, the input is decomposed, upon a successful match, into a tuple of three elements. The first element represents the optional target object, which is present if the target is an instance method. The second element represents the generic type instantiation, which is non-empty if the target is a generic instantiation. The third element represents the arguments to the function or method.  
  
## Remarks  
 This function is named `SpecificCallPattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.DerivedPatterns Module (F#)](../vs140/Quotations.DerivedPatterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)