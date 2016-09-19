---
title: "Expr.ToString Method (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d8e236c6-adee-4620-9361-fd217d09052d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expr.ToString Method (F#)
Formats the expression as a string.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Quotations  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.ToString : bool -> string  
  
// Usage:  
expr.ToString (full)  
```  
  
#### Parameters  
 `full`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 Indicates whether or not method, property, constructor and type objects should be printed in detail. If false, these are abbreviated to their names.  
  
## Return Value  
 The formatted string.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Quotations.Expr Class (F#)](../Topic/Quotations.Expr%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Quotations Namespace (F#)](../Topic/Microsoft.FSharp.Quotations%20Namespace%20\(F%23\).md)