---
title: "Array3D.zeroCreate&lt;&#39;T&gt; Function (F#)"
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
  - Array3D.zeroCreate<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a56ae875-8805-4527-b459-a7a97756ce84
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array3D.zeroCreate&lt;&#39;T&gt; Function (F#)
Creates an array where the entries are initially the default value.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array3D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array3D.zeroCreate : int -> int -> int -> 'T [,,]  
  
// Usage:  
Array3D.zeroCreate length1 length2 length3  
```  
  
#### Parameters  
 `length1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the first dimension.  
  
 `length2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the second dimension.  
  
 `length3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the third dimension.  
  
## Return Value  
 The created array.  
  
## Remarks  
 This function is named `ZeroCreate` in compiled assembly. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array3D Module (F#)](../vs140/Collections.Array3D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)