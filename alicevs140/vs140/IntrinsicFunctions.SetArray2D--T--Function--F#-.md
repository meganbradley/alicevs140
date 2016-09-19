---
title: "IntrinsicFunctions.SetArray2D&lt;&#39;T&gt; Function (F#)"
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
  - IntrinsicFunctions.SetArray2D<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fa4f965b-abe3-44ad-9244-0d47c3858292
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicFunctions.SetArray2D&lt;&#39;T&gt; Function (F#)
The standard overloaded associative (2-indexed) mutation operator  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicFunctions  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
SetArray2D : 'T [,] -> int -> int -> 'T -> unit  
  
// Usage:  
SetArray2D target index1 index2 value  
```  
  
#### Parameters  
 `target`  
 Type: `'T` [&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 A two-dimensional array.  
  
 `index1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 An index along the first dimension.  
  
 `index2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 An index along the second dimension.  
  
 `value`  
 Type: `'T`  
  
 The new value to set at the specified indices.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.IntrinsicFunctions Module (F#)](../vs140/LanguagePrimitives.IntrinsicFunctions-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)