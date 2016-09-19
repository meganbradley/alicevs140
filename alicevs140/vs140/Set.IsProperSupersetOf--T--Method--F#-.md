---
title: "Set.IsProperSupersetOf&lt;&#39;T&gt; Method (F#)"
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
  - Set.IsProperSupersetOf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 4c2a373c-8a5b-494b-94a7-004a5f1333be
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.IsProperSupersetOf&lt;&#39;T&gt; Method (F#)
Evaluates to `true` if all elements of the second set are in the first, and at least one element of the first is not in the second.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.IsProperSupersetOf : Set<'T> -> bool (requires comparison)  
  
// Usage:  
set.IsProperSupersetOf (otherSet)  
```  
  
#### Parameters  
 `otherSet`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The set to test against.  
  
## Return Value  
 `true` if this set is a proper superset of `otherSet`. Otherwise, returns `false`.  
  
## Remarks  
  
## Example  
 The following code illustrates the use of the `IsProperSupersetOf` method.  
  
 [!CODE [FsSets#8](../CodeSnippet/VS_Snippets_Fsharp/fssets#8)]  
  
 **Output**  
  
 **set [1; 2; 3; 4; 5; 6; 7; 8; 9] is a proper superset of set [1; 2; 3; 4; 5; 6]: trueset [1; 2; 3; 4; 5; 6] is a proper superset of set [1; 2; 3; 4; 5; 6]: falseset [5; 6; 7; 8; 9; 10] is a proper superset of set [1; 2; 3; 4; 5; 6]: false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set<'T> Class (F#)](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)