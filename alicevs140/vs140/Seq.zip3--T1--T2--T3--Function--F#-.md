---
title: "Seq.zip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)"
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
  - Seq.zip3<'T1,'T2,'T3>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ef13bebb-22ae-4eb9-873b-87dd29154d16
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.zip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)
Combines the three sequences into a list of triples. The sequences need not have equal lengths: when one sequence is exhausted any remaining elements in the other sequences are ignored.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Seq.zip3 : seq<'T1> -> seq<'T2> -> seq<'T3> -> seq<'T1 * 'T2 * 'T3>  
  
// Usage:  
Seq.zip3 source1 source2 source3  
```  
  
#### Parameters  
 `source1`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T1>`  
  
 The first input sequence.  
  
 `source2`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T2>`  
  
 The second input sequence.  
  
 `source3`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T3>`  
  
 The third input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when any of the input sequences is null.|  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 This function is named `Zip3` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)