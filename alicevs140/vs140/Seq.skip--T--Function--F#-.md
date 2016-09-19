---
title: "Seq.skip&lt;&#39;T&gt; Function (F#)"
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
  - Seq.skip<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b4eb3f08-8594-4d17-8180-852c6c688bf1
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.skip&lt;&#39;T&gt; Function (F#)
Returns a sequence that skips N elements of the underlying sequence and then yields the remaining elements of the sequence.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.skip : int -> seq<'T> -> seq<'T>  
  
// Usage:  
Seq.skip count source  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of items to skip.  
  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input sequence is null.|  
|<xref:System.InvalidOperationException?qualifyHint=False>|Thrown when count exceeds the number of elements in the sequence.|  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 This function is named `Skip` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Seq.skip` to skip the first five squares of a list of squares.  
  
 [!CODE [FsSequences#171](../CodeSnippet/VS_Snippets_Fsharp/fssequences#171)]  
  
 **36 49 64 81 100**    
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)