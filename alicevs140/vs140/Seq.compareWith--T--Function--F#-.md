---
title: "Seq.compareWith&lt;&#39;T&gt; Function (F#)"
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
  - Seq.compareWith<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5a740135-0b3a-4545-816f-8f91cc31290f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.compareWith&lt;&#39;T&gt; Function (F#)
Compares two sequences using the given comparison function, element by element.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.compareWith : ('T -> 'T -> int) -> seq<'T> -> seq<'T> -> int  
  
// Usage:  
Seq.compareWith comparer source1 source2  
```  
  
#### Parameters  
 `comparer`  
 Type: `'T -> 'T ->` [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 A function that takes an element from each sequence and returns an int. If it evaluates to a non-zero value iteration is stopped and that value is returned.  
  
 `source1`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The first input sequence.  
  
 `source2`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The second input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when either of the input sequences is null.|  
  
## Return Value  
 Returns the first non-zero result from the comparison function. If the end of a sequence is reached it returns a -1 if the first sequence is shorter and a 1 if the second sequence is shorter.  
  
## Remarks  
 This function is named `CompareWith` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Seq.compareWith` to compare two sequences using a custom comparison function.  
  
 [!CODE [FsSequences#19](../CodeSnippet/VS_Snippets_Fsharp/fssequences#19)]  
  
 **Sequence1 is less than sequence2.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)