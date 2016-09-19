---
title: "Array.fold&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - Array.fold<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5ed9dd3b-3694-4567-94d0-fd9a24474e09
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.fold&lt;&#39;T,&#39;State&gt; Function (F#)
Applies a function to each element of the collection, threading an accumulator argument through the computation. If the input function is `f` and the elements are `i0...iN` then computes `f (... (f s i0)...) iN.`  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.fold : ('State -> 'T -> 'State) -> 'State -> 'T [] -> 'State  
  
// Usage:  
Array.fold folder state array  
```  
  
#### Parameters  
 `folder`  
 Type: `'State -> 'T -> 'State`  
  
 The function to update the state given the input elements.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The final state.  
  
## Remarks  
 This function is named `Fold` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.fold`.  
  
 [!CODE [FsArrays#32](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#32)]  
  
 **Output**  
  
 **Sum of the elements of array [1; 2; 3] is 6.**  
**Array [&#124;1; 1; 1&#124;] average: 1.000000 stddev: 0.000000**  
**Array [&#124;1; 2; 1&#124;] average: 1.333333 stddev: 0.471405**  
**Array [&#124;1; 2; 3&#124;] average: 2.000000 stddev: 0.816497**  
**0.0**  
**1.0**  
**2.5**  
**5.1**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)