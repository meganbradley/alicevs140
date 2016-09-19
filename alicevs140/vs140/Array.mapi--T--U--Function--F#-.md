---
title: "Array.mapi&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Array.mapi<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f7e45994-b0a1-49e6-8fb5-5641cea8fde4
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.mapi&lt;&#39;T,&#39;U&gt; Function (F#)
Builds a new array whose elements are the results of applying the given function to each of the elements of the array. The integer index passed to the function indicates the index of element being transformed.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.mapi : (int -> 'T -> 'U) -> 'T [] -> 'U []  
  
// Usage:  
Array.mapi mapping array  
```  
  
#### Parameters  
 `mapping`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T -> 'U`  
  
 The function to transform elements and their indices.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The array of transformed elements.  
  
## Remarks  
 This function is named `MapIndexed` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code demonstrates the use of `Array.mapi`.  
  
 [!CODE [FsArrays#53](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#53)]  
  
 **Output**  
  
 **[&#124;(0, 1); (1, 2); (2, 3)&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)