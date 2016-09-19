---
title: "Seq.initInfinite&lt;&#39;T&gt; Function (F#)"
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
  - Seq.initInfinite<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d1804e53-da92-48ec-8d6e-57eaf4c62bef
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.initInfinite&lt;&#39;T&gt; Function (F#)
Generates a new sequence which, when iterated, will return successive elements by calling the given function.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Seq  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.initInfinite : (int -> 'T) -> seq<'T>  
  
// Usage:  
Seq.initInfinite initializer  
```  
  
#### Parameters  
 `initializer`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T`  
  
 A function that generates an item in the sequence from a given index.  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 The results of calling the function will not be saved, that is the function will be reapplied as necessary to regenerate the elements. The function is passed the index of the item being generated.  
  
 Iteration can continue up to `Int32.MaxValue`.  
  
 This function is named `InitializeInfinite` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Thread Safety  
 The returned sequence may be passed between threads safely. However, individual `IEnumerator` values generated from the returned sequence should not be accessed concurrently.  
  
## Example  
 The following example shows the use of `Seq.initInfinite` to create a sequence `1/n^2`, with alternating signs.  
  
 [!CODE [FsSequences#13](../CodeSnippet/VS_Snippets_Fsharp/fssequences#13)]  
  
 **seq [-1.0; 0.25; -0.1111111111; 0.0625; ...]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)