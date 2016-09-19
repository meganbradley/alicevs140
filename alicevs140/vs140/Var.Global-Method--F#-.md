---
title: "Var.Global Method (F#)"
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
  - FSharpVar.Global
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2c46e73b-199e-42b2-aeca-8bd363cee8ef
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Var.Global Method (F#)
Fetches or creates a new variable with the given name and type from a global pool of shared variables indexed by name and type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Global : string * Type -> Var  
  
// Usage:  
Var.Global (name, typ)  
```  
  
#### Parameters  
 `name`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The name of the variable.  
  
 `typ`  
 Type: <xref:System.Type?qualifyHint=False>  
  
 The type associated with the variable.  
  
## Return Value  
 The retrieved or created variable.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Var Class (F#)](../vs140/Quotations.Var-Class--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)