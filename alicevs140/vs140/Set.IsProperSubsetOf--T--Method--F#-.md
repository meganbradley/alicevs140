---
title: "Set.IsProperSubsetOf&lt;&#39;T&gt; Method (F#)"
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
  - Set.IsProperSubsetOf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: bd0a671b-51ff-4c9e-b2fb-5089244750f5
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.IsProperSubsetOf&lt;&#39;T&gt; Method (F#)
Evaluates to `true` if all elements of the first set are in the second, and at least one element of the second is not in the first.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.IsProperSubsetOf : Set<'T> -> bool (requires comparison)  
  
// Usage:  
set.IsProperSubsetOf (otherSet)  
```  
  
#### Parameters  
 `otherSet`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The set to test against.  
  
## Return Value  
 `true` if this set is a proper subset of `otherSet`. Otherwise, returns `false`.  
  
## Remarks  
  
## Example  
 The following code illustrates the use of the `IsProperSubsetOf` method.  
  
 [!CODE [FsSets#6](../CodeSnippet/VS_Snippets_Fsharp/fssets#6)]  
  
 **Output**  
  
 **set [1; 2; 3; 4; 5] is a proper subset of set [1; 2; 3; 4; 5; 6]: trueset [1; 2; 3; 4; 5; 6] is a proper subset of set [1; 2; 3; 4; 5; 6]: falseset [5; 6; 7; 8; 9; 10] is a proper subset of set [1; 2; 3; 4; 5; 6]: false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set<'T> Class (F#)](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)