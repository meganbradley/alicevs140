---
title: "Seq.init&lt;&#39;T&gt; Function (F#)"
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
  - Seq.init<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 059de69d-812c-4f8e-be86-88aa72101576
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.init&lt;&#39;T&gt; Function (F#)
Generates a new sequence which, when iterated, will return successive elements by calling the given function, up to the given count.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Seq  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.init : int -> (int -> 'T) -> seq<'T>  
  
// Usage:  
Seq.init count initializer  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The maximum number of items to generate for the sequence.  
  
 `initializer`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T`  
  
 A function that generates an item in the sequence from a given index.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when count is negative.|  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 Each element is saved after its initialization. The function is passed the index of the item being generated.  
  
 This function is named `Initialize` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Thread Safety  
 The returned sequence may be passed between threads safely. However, individual `IEnumerator` values generated from the returned sequence should not be accessed concurrently.  
  
## Example  
 The following example demonstrates the use of `Seq.init` to create a sequence of the first five multiples of 10.  
  
 [!CODE [FsSequences#10](../CodeSnippet/VS_Snippets_Fsharp/fssequences#10)]  
  
 **0 10 20 30 40**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)