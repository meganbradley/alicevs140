---
title: "Array.sortWith&lt;&#39;T&gt; Function (F#)"
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
  - Array.sortWith<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 699d3638-4244-4f42-8496-45f53d43ce95
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.sortWith&lt;&#39;T&gt; Function (F#)
Sorts the elements of an array, using the given comparison function as the order, returning a new array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.sortWith : ('T -> 'T -> int) -> 'T [] -> 'T []  
  
// Usage:  
Array.sortWith comparer array  
```  
  
#### Parameters  
 `comparer`  
 Type: `'T -> 'T ->`[int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The function to compare pairs of array elements.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The sorted array.  
  
## Remarks  
 This is not a stable sort, that is, the original order of equal elements might not be preserved. For a stable sort, consider using [Seq.sort](../vs140/Seq.sort--T--Function--F#-.md).  
  
 This function is named `SortWith` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows the use of **Array.sortWith**.  
  
 [!CODE [FsArrays#65](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#65)]  
  
 **Output**  
  
 **Before sorting:**   
**[&#124;"<>"; "&"; "&&"; "&&&"; "<"; ">"; "&#124;"; "&#124;&#124;"; "&#124;&#124;&#124;"&#124;]**  
**After sorting:**   
**[&#124;"&"; "&#124;"; "<"; ">"; "&&"; "&#124;&#124;"; "<>"; "&&&"; "&#124;&#124;&#124;"&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)