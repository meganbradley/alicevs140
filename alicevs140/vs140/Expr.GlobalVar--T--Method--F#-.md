---
title: "Expr.GlobalVar&lt;&#39;T&gt; Method (F#)"
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
  - FSharpExpr.GlobalVar<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: eefa478a-0d37-4119-a221-2bfa0e1e7b3c
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.GlobalVar&lt;&#39;T&gt; Method (F#)
Fetches or creates a new variable with the given name and type from a global pool of shared variables indexed by name and type. The type is given by the expicit or inferred type parameter.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member GlobalVar : string -> Expr<'T>  
  
// Usage:  
Expr.GlobalVar (name)  
```  
  
#### Parameters  
 `name`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The variable name.  
  
## Return Value  
 The created of fetched typed global variable.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Expr Class (F#)](../Topic/Quotations.Expr%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)