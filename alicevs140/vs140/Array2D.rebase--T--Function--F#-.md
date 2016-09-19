---
title: "Array2D.rebase&lt;&#39;T&gt; Function (F#)"
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
  - Array2D.rebase<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5fc9b6f1-ef54-49bc-aa70-17624490a53d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array2D.rebase&lt;&#39;T&gt; Function (F#)
Creates a new array whose elements are the same as the input array but where a non-zero-based input array generates a corresponding zero-based output array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array2D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array2D.rebase : 'T [,] -> 'T [,]  
  
// Usage:  
Array2D.rebase array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The input array.  
  
## Return Value  
 The zero-based output array.  
  
## Remarks  
 This function is named `Rebase` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array2D Module (F#)](../vs140/Collections.Array2D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)