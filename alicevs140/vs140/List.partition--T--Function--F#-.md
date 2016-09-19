---
title: "List.partition&lt;&#39;T&gt; Function (F#)"
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
  - List.partition<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: aba8252d-ba85-4ec2-a2e2-930276e63a63
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.partition&lt;&#39;T&gt; Function (F#)
Splits the collection into two collections, containing the elements for which the given predicate returns `true` and `false` respectively.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.partition : ('T -> bool) -> 'T list -> 'T list * 'T list  
  
// Usage:  
List.partition predicate list  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 A list containing the elements for which the predicate evaluated to `false` and a list containing the elements for which the predicate evaluated to `true`.  
  
## Remarks  
 This function is named `Partition` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use `List.partition`.  
  
 [!CODE [FsLists#50](../CodeSnippet/VS_Snippets_Fsharp/fslists#50)]  
  
 **Output**  
  
 **Evens: [2; 4; 6; 8; 10]**  
**Odds: [1; 3; 5; 7; 9]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)