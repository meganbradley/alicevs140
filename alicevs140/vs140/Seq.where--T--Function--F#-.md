---
title: "Seq.where&lt;&#39;T&gt; Function (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e6b5bf50-4716-423c-98fe-f77d03bb6f7f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Seq.where&lt;&#39;T&gt; Function (F#)
Returns a new collection containing only the elements of the collection for which the given predicate returns `true`.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Seq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:where : ('T -> bool) -> seq<'T> -> seq<'T>// Usage:Seq.where predicate source  
```  
  
#### Parameters  
 `predicate`  
 Type: 'T -> [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 A function to test whether each item in the input sequence should be included in the output.  
  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)<'T>  
  
 The input sequence.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentNullException?qualifyHint=False>|Thrown when the input sequence is null.|  
  
## Return Value  
 The result sequence.  
  
## Remarks  
 The returned sequence may be passed between threads safely. However, individual <xref:System.Collections.Generic.IEnumerator`1?qualifyHint=False> values generated from the returned sequence should not be accessed concurrently. Remember that sequence is subject to lazy evaluation, which means that effects are delayed until it is enumerated. This function is a synonym for [Seq.filter](../Topic/Seq.filter%3C'T%3E%20Function%20\(F%23\).md).  
  
 This function is named `Where` in the .NET assembly. If accessing the member from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
 .0  
  
## See Also  
 [Collections.Seq Module (F#)](../Topic/Collections.Seq%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)   
 [Seq.filter<'T> Function (F#)](../Topic/Seq.filter%3C'T%3E%20Function%20\(F%23\).md)