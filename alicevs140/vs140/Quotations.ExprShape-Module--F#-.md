---
title: "Quotations.ExprShape Module (F#)"
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
  - Quotations.ExprShape
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7685150e-2432-4d39-9338-57292eff18de
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Quotations.ExprShape Module (F#)
Active patterns for traversing, visiting, rebuilding and transforming expressions in a generic way  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module ExprShape  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[RebuildShapeCombination](../vs140/ExprShape.RebuildShapeCombination-Function--F#-.md)  `: obj * Expr list -> Expr`|Rebuild combination expressions. The first parameter should be an object returned by the [ShapeCombination](../vs140/ExprShape.ShapeVar-ShapeLambda-ShapeCombination-Active-Pattern--F#-.md) case of the active pattern in this module.|  
  
## Active Patterns  
  
|Active Pattern|Description|  
|--------------------|-----------------|  
|[( &#124;ShapeVar&#124;ShapeLambda&#124;ShapeCombination&#124; )](../vs140/ExprShape.ShapeVar-ShapeLambda-ShapeCombination-Active-Pattern--F#-.md)|An active pattern that performs a complete decomposition viewing the expression tree as a binding structure|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)