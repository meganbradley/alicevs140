---
title: "DerivedPatterns.Single Active Pattern (F#)"
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
  - DerivedPatterns.( |Single|_| )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 02a25920-18c4-491e-9a80-efd0212b99bc
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DerivedPatterns.Single Active Pattern (F#)
Recognizes constant 32-bit floating point number expressions.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations.DerivedPatterns  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( |Single|_| ) : (input:Expr) -> float32 option  
```  
  
#### Parameters  
 `input`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The input expression to match against.  
  
## Return Value  
 The result of a successful match is the value as a `single`.  
  
## Remarks  
 This function is named `SinglePattern` in the .NET Framework assembly. If you are accessing the member from a .NET Framework language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.DerivedPatterns Module (F#)](../vs140/Quotations.DerivedPatterns-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)