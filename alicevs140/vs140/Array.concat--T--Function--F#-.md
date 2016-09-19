---
title: "Array.concat&lt;&#39;T&gt; Function (F#)"
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
  - Array.concat<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f7219b79-1ec8-4a25-96b1-edbedb358302
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.concat&lt;&#39;T&gt; Function (F#)
Builds a new array that contains the elements of each of the given sequence of arrays.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.concat : seq<'T []> -> 'T []  
  
// Usage:  
Array.concat arrays  
```  
  
#### Parameters  
 `arrays`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)`>`  
  
 The input sequence of arrays.  
  
## Return Value  
 The concatenation of the sequence of input arrays.  
  
## Remarks  
 This function is named `Concat` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Array.concat`.  
  
 [!CODE [FsArrays#16](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#16)]  
  
 **[&#124;(1, 1, 1); (1, 2, 2); (1, 3, 3); (2, 1, 2); (2, 2, 4); (2, 3, 6);**  
 **(3, 1, 3); (3, 2, 6); (3, 3, 9)&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)