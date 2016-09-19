---
title: "Quotations.Expr&lt;&#39;T&gt; Class (F#)"
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
  - Quotations.FSharpExpr<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 975ca4d3-ac2b-46db-9f01-23cf8b190c6e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Quotations.Expr&lt;&#39;T&gt; Class (F#)
Type-carrying quoted expressions. Expressions are generated either by quotations in source text or programmatically  
  
 **Namespace/Module Path:** Microsoft.FSharp.Quotations  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
type Expr<'T> =  
 class  
  member this.Raw :  Expr  
 end  
```  
  
## Remarks  
 This type is named `FSharpExpr` in the assembly. If you are accessing the type from a language other than F#, or through reflection, use this name.  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Raw](../vs140/Expr.Raw--T--Property--F#-.md)|Gets the raw expression associated with this type-carrying expression|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)