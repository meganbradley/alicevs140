---
title: "Array.permute&lt;&#39;T&gt; Function (F#)"
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
  - Array.permute<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d89598b7-7a90-4746-80b5-ff5de4ba56a8
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.permute&lt;&#39;T&gt; Function (F#)
Returns an array with all elements permuted according to the specified permutation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.permute : (int -> int) -> 'T [] -> 'T []  
  
// Usage:  
Array.permute indexMap array  
```  
  
#### Parameters  
 `indexMap`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The function that maps input indices to output indices.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The permuted array.  
  
## Remarks  
 This function is named `Permute` in compiled assemblies. If accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.permute`.  
  
 [!CODE [FsArrays#34](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#34)]  
  
 **Output**  
  
 **[&#124;1; 2; 3; 4; 5&#124;]**  
**[&#124;5; 1; 2; 3; 4&#124;]**  
**[&#124;4; 5; 1; 2; 3&#124;]**  
**[&#124;3; 4; 5; 1; 2&#124;]**  
**[&#124;2; 3; 4; 5; 1&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)