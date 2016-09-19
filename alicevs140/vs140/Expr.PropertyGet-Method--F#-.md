---
title: "Expr.PropertyGet Method (F#)"
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
  - FSharpExpr.PropertyGet
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 403fa57a-f195-464d-aa2e-20b201c5948a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.PropertyGet Method (F#)
Creates an expression that represents reading a static property  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:  
static member PropertyGet : PropertyInfo * ?Expr list -> Expr  
static member PropertyGet : Expr * PropertyInfo * ?Expr list -> Expr  
  
// Usage:  
Expr.PropertyGet (property)  
Expr.PropertyGet (property, indexerArgs = indexerArgs)  
Expr.PropertyGet (obj, property)  
Expr.PropertyGet (obj, property, indexerArgs = indexerArgs)  
```  
  
#### Parameters  
 `property`  
 Type: <xref:System.Reflection.PropertyInfo?qualifyHint=False>  
  
 The description of the property.  
  
 `indexerArgs`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 List of indices for the property if it is an indexed property.  
  
 `obj`  
 Type: [Expr](../Topic/Quotations.Expr%20Class%20\(F%23\).md)  
  
 The object instance, if applicable.  
  
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