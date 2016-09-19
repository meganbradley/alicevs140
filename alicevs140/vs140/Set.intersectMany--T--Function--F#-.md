---
title: "Set.intersectMany&lt;&#39;T&gt; Function (F#)"
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
  - Set.intersectMany<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2a0a9352-205f-4ea2-9b4c-c58f73a8e784
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.intersectMany&lt;&#39;T&gt; Function (F#)
Computes the intersection of a sequence of sets. The sequence must be non-empty.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Set  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.intersectMany : seq<Set<'T>> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.intersectMany sets  
```  
  
#### Parameters  
 `sets`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<`[Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>>`  
  
 The sequence of sets to intersect.  
  
## Return Value  
 The intersection of the input sets.  
  
## Remarks  
 This function is named `IntersectMany` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of the `Set.intersectMany` function.  
  
 [!CODE [FsSets#5](../CodeSnippet/VS_Snippets_Fsharp/fssets#5)]  
  
 **Output**  
  
 **Numbers between 1 and 10,000 that are divisible by**   
**all the numbers from 1 to 9:**  
**set [2520; 5040; 7560]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)