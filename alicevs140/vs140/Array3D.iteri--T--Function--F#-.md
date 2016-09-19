---
title: "Array3D.iteri&lt;&#39;T&gt; Function (F#)"
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
  - Array3D.iteri<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c4e1d5ec-7b6e-4aa3-9fab-d1ff443ee867
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array3D.iteri&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the array. The integer indicies passed to the function indicates the index of element.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array3D  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array3D.iteri : (int -> int -> int -> 'T -> unit) -> 'T [,,] -> unit  
  
// Usage:  
Array3D.iteri action array  
```  
  
#### Parameters  
 `action`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T ->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to apply to each element of the array.  
  
 `array`  
 Type: `'T`[&#91;,,&#93;](../Topic/Core.%3C'T%3E%20Type%20\(F%23\)3.md)  
  
 The input array.  
  
## Remarks  
 This function is named `IterateIndexed` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array3D Module (F#)](../vs140/Collections.Array3D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)