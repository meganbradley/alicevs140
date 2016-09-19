---
title: "Seq.reduce&lt;&#39;T&gt; Function (F#)"
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
  - Seq.reduce<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a2ad4f64-ac69-47d2-92f0-7173d9dfeae9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.reduce&lt;&#39;T&gt; Function (F#)
Applies a function to each element of the sequence, threading an accumulator argument through the computation. This function begins by applying the function to the first two elements. It then passes this result into the function along with the third element and so on. The function returns the final result.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.reduce : ('T -> 'T -> 'T) -> seq<'T> -> 'T  
  
// Usage:  
Seq.reduce reduction source  
```  
  
#### Parameters  
 `reduction`  
 Type: `'T -> 'T -> 'T`  
  
 A function that takes in the current accumulated result and the next element of the sequence to produce the next accumulated result.  
  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input sequence is empty.|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input sequence is null.|  
  
## Return Value  
 The result of the computation.  
  
## Remarks  
 This function is named `Reduce` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)