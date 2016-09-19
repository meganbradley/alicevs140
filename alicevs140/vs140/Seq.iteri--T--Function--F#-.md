---
title: "Seq.iteri&lt;&#39;T&gt; Function (F#)"
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
  - Seq.iteri<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e5479c37-bdc8-465d-8c2a-2f677269c22b
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.iteri&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the collection. The integer passed to the function indicates the index of element.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.iteri : (int -> 'T -> unit) -> seq<'T> -> unit  
  
// Usage:  
Seq.iteri action source  
```  
  
#### Parameters  
 `action`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T ->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 A function to apply to each element of the sequence that can also access the current index.  
  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input sequence is null.|  
  
## Remarks  
 This function is named `IterateIndexed` in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Seq.iteri` and compares its behavior to related functions.  
  
 [!CODE [FsSequences#43](../CodeSnippet/VS_Snippets_Fsharp/fssequences#43)]  
  
 **Output**  
  
 **Seq.iter: element is 1**  
**Seq.iter: element is 2**  
**Seq.iter: element is 3**  
**Seq.iteri: element 0 is 1**  
**Seq.iteri: element 1 is 2**  
**Seq.iteri: element 2 is 3**  
**Seq.iter2: elements are 1 4**  
**Seq.iter2: elements are 2 5**  
**Seq.iter2: elements are 3 6**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)