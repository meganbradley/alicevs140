---
title: "Array3D.map&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Array3D.map<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 01f91430-9fb0-4fa3-bc7f-dbfd004487af
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array3D.map&lt;&#39;T,&#39;U&gt; Function (F#)
Creates a new array whose elements are the results of applying the given function to each of the elements of the array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array3D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array3D.map : ('T -> 'U) -> 'T [,,] -> 'U [,,]  
  
// Usage:  
Array3D.map mapping array  
```  
  
#### Parameters  
 `mapping`  
 Type: `'T -> 'U`  
  
 The function to transform each element of the array.  
  
 `array`  
 Type: `'T` [&#91;,,&#93;](../Topic/Core.%3C'T%3E%20Type%20\(F%23\)3.md)  
  
 The input array.  
  
## Return Value  
 The array created from the transformed elements.  
  
## Remarks  
 For non-zero-based arrays the basing on an input array will be propagated to the output array.  
  
 This function is named `Map` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array3D Module (F#)](../vs140/Collections.Array3D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)