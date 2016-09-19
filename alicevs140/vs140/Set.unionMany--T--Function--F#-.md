---
title: "Set.unionMany&lt;&#39;T&gt; Function (F#)"
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
  - Set.unionMany<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 0b4b238d-9393-4f23-8bed-7986a0177820
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.unionMany&lt;&#39;T&gt; Function (F#)
Computes the union of a sequence of sets.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.unionMany : seq<Set<'T>> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.unionMany sets  
```  
  
#### Parameters  
 `sets`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<`[Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>>`  
  
 The sequence of sets to union.  
  
## Return Value  
 The union of the input sets.  
  
## Remarks  
 This function is named `UnionMany` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of the `Set.unionMany` function.  
  
 [!CODE [FsSets#15](../CodeSnippet/VS_Snippets_Fsharp/fssets#15)]  
  
 **Output**  
  
 **Numbers up to 40 that are multiples of numbers from 2 to 5:**  
**2 3 4 5 6 8 9 10 12 14 15 16 18 20 21 22 24 25 26 27 28 30 32 33 34 35 36 38 39 40**    
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)