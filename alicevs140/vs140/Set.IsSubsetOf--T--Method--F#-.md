---
title: "Set.IsSubsetOf&lt;&#39;T&gt; Method (F#)"
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
  - Set.IsSubsetOf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2069807c-c9fe-403f-b51c-0edc043ed796
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.IsSubsetOf&lt;&#39;T&gt; Method (F#)
Evaluates to `true` if all elements of the first set are in the second.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.IsSubsetOf : Set<'T> -> bool (requires comparison)  
  
// Usage:  
set.IsSubsetOf (otherSet)  
```  
  
#### Parameters  
 `otherSet`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The set to test against.  
  
## Return Value  
 `true` if this set is a subset of `otherSet`. Otherwise, returns `false`.  
  
## Remarks  
  
## Example  
 The following code illustrates the use of the `IsSubsetOf` method.  
  
 [!CODE [FsSets#10](../CodeSnippet/VS_Snippets_Fsharp/fssets#10)]  
  
 **Output**  
  
 **set [1; 2; 3; 4; 5] is a subset of set [1; 2; 3; 4; 5; 6]: trueset [1; 2; 3; 4; 5; 6] is a subset of set [1; 2; 3; 4; 5; 6]: trueset [5; 6; 7; 8; 9; 10] is a subset of set [1; 2; 3; 4; 5; 6]: true**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set<'T> Class (F#)](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)