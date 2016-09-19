---
title: "IntrinsicFunctions.SetArray4D&lt;&#39;T&gt; Function (F#)"
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
  - IntrinsicFunctions.SetArray4D<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 20f10348-37d2-43c2-ab77-81dfd6745494
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicFunctions.SetArray4D&lt;&#39;T&gt; Function (F#)
The standard overloaded associative (4-indexed) mutation operator.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicFunctions  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
SetArray4D : 'T [,,,] -> int -> int -> int -> int -> 'T -> unit  
  
// Usage:  
SetArray4D target index1 index2 index3 index4 value  
```  
  
#### Parameters  
 `target`  
 Type: `'T` [&#91;,,,&#93;](../vs140/Core.--T--Type--F#-1.md)  
  
 A four-dimensional array.  
  
 `index1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the first dimension.  
  
 `index2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the second dimension.  
  
 `index3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the third dimension.  
  
 `index4`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the fourth dimension.  
  
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