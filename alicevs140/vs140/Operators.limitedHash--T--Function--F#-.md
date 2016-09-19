---
title: "Operators.limitedHash&lt;&#39;T&gt; Function (F#)"
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
  - Operators.limitedHash<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 499fba7c-6b04-47e7-aeda-05420e6e2d21
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.limitedHash&lt;&#39;T&gt; Function (F#)
A generic hash function. This function has the same behavior as [hash](../Topic/Operators.hash%3C'T%3E%20Function%20\(F%23\).md), however the default structural hashing for F# union, record and tuple types stops when the given limit of nodes is reached. The exact behavior of the function can be adjusted on a type-by-type basis by implementing <xref:System.Object.GetHashCode?qualifyHint=False> for each type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
limitedHash : int -> 'T -> int (requires equality)  
  
// Usage:  
limitedHash limit obj  
```  
  
#### Parameters  
 `limit`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The limit of nodes.  
  
 `obj`  
 Type: `'T`  
  
 The input object.  
  
## Return Value  
 The computed hash.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)