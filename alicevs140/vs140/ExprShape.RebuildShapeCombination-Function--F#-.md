---
title: "ExprShape.RebuildShapeCombination Function (F#)"
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
  - ExprShape.RebuildShapeCombination
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 38c3f403-b3ed-4ddf-a69c-53a21339aa2f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ExprShape.RebuildShapeCombination Function (F#)
Re-build combination expressions. The first parameter should be an object returned by the `ShapeCombination` case of the active pattern in this module.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations.ExprShape  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RebuildShapeCombination : obj * Expr list -> Expr  
  
// Usage:  
RebuildShapeCombination (shape, arguments)  
```  
  
#### Parameters  
 `shape`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The input shape.  
  
 `arguments`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The list of arguments.  
  
## Return Value  
 The rebuilt expression.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.ExprShape Module (F#)](../vs140/Quotations.ExprShape-Module--F#-.md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)