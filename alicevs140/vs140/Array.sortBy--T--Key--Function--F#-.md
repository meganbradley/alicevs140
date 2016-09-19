---
title: "Array.sortBy&lt;&#39;T,&#39;Key&gt; Function (F#)"
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
  - Array.sortBy<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 144498dc-091d-4575-a229-c0bcbd61426b
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.sortBy&lt;&#39;T,&#39;Key&gt; Function (F#)
Sorts the elements of an array, using the given projection for the keys and returning a new array. Elements are compared using [Operators.compare](../vs140/Operators.compare--T--Function--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.sortBy : ('T -> 'Key) -> 'T [] -> 'T [] (requires comparison)  
  
// Usage:  
Array.sortBy projection array  
```  
  
#### Parameters  
 `projection`  
 Type: `'T -> 'Key`  
  
 The function to transform array elements into the type that is compared.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The sorted array.  
  
## Remarks  
 This is not a stable sort, that is, the original order of equal elements is not necessarily preserved. For a stable sort, consider using [Seq.sort](../vs140/Seq.sort--T--Function--F#-.md).  
  
 This function is named `SortBy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.sortBy`.  
  
 [!CODE [FsArrays#38](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#38)]  
  
 **Output**  
  
 **[&#124;1; -2; 4; 5; 8&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)