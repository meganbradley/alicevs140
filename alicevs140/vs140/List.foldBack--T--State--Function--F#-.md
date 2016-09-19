---
title: "List.foldBack&lt;&#39;T,&#39;State&gt; Function (F#)"
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
  - List.foldBack<'T,'State>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b9a58e66-efe1-445f-a90c-ac9ffb9d40c7
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.foldBack&lt;&#39;T,&#39;State&gt; Function (F#)
Applies a function to each element of the collection, threading an accumulator argument through the computation. If the input function is `f` and the elements are `i0...iN`, then this function computes `f i0 (...(f iN s))`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.foldBack : ('T -> 'State -> 'State) -> 'T list -> 'State -> 'State  
  
// Usage:  
List.foldBack folder list state  
```  
  
#### Parameters  
 `folder`  
 Type: `'T -> 'State -> 'State`  
  
 The function to update the state given the input elements.  
  
 `list`  
 Type: `'T` [list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
 `state`  
 Type: `'State`  
  
 The initial state.  
  
## Return Value  
 The final state value.  
  
## Remarks  
 This function is named `FoldBack` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.foldBack`.  
  
 [!CODE [FsLists#41](../CodeSnippet/VS_Snippets_Fsharp/fslists#41)]  
  
 **Output**  
  
 **6**  
**[1; 2; 3; 4; 5; 6; 7; 8; 9; 10]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)