---
title: "Expr.Value Method (F#)"
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
  - FSharpExpr.Value
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ffae1099-0e49-4e54-9110-cb625954e667
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.Value Method (F#)
Creates an expression that represents a constant value of a particular type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Value : obj * Type -> Expr  
  
// Usage:  
Expr.Value (value, expressionType)  
```  
  
#### Parameters  
 `value`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The object.  
  
 `expressionType`  
 Type: <xref:System.Type?qualifyHint=False>  
  
 The type of the object.  
  
## Return Value  
 The resulting expression.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Expr Class (F#)](../Topic/Quotations.Expr%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)