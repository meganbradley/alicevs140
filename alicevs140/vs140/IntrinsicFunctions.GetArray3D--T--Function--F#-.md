---
title: "IntrinsicFunctions.GetArray3D&lt;&#39;T&gt; Function (F#)"
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
  - IntrinsicFunctions.GetArray3D<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e3d39923-e6f1-4a14-8dfc-afc15f1b89da
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicFunctions.GetArray3D&lt;&#39;T&gt; Function (F#)
The standard overloaded associative (3-indexed) lookup operator.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicFunctions  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GetArray3D : 'T [,,] -> int -> int -> int -> 'T  
  
// Usage:  
GetArray3D source index1 index2 index3  
```  
  
#### Parameters  
 `source`  
 Type: `'T`[&#91;,,&#93;](../Topic/Core.%3C'T%3E%20Type%20\(F%23\)3.md)  
  
 The input array.  
  
 `index1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The first index.  
  
 `index2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The second index.  
  
 `index3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The third index.  
  
## Return Value  
 The value in the array at the specified indices.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.IntrinsicFunctions Module (F#)](../vs140/LanguagePrimitives.IntrinsicFunctions-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)