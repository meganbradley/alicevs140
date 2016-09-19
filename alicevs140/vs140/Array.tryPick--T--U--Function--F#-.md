---
title: "Array.tryPick&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Array.tryPick<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 72d45f85-037b-43a9-97fd-17239f72713e
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.tryPick&lt;&#39;T,&#39;U&gt; Function (F#)
Applies the given function to successive elements, returning the first result where function returns `Some`. If the function does not return `Some` for any element, then `None` is returned.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.tryPick : ('T -> 'U option) -> 'T [] -> 'U option  
  
// Usage:  
Array.tryPick chooser array  
```  
  
#### Parameters  
 `chooser`  
 Type: `'T -> 'U option`  
  
 The function to transform the array elements into options.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The first transformed element that has an option value of `Some`, or `None` if the function does not return `Some` for any element.  
  
## Remarks  
 This function is named `TryPick` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Array.tryPick` to attempt to locate an element that satisfies a condition, and also return some additional data about the element, in this case the square root and the cube root.  
  
 [!CODE [FsArrays#27](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#27)]  
  
 **Found an element 1 with square root 1 and cube root 1.**  
**Found an element 64 with square root 8 and cube root 4.**  
**Found an element 729 with square root 27 and cube root 9.**  
**Found an element 4096 with square root 64 and cube root 16.**  
**Did not find an element that is both a perfect square and a perfect cube.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)