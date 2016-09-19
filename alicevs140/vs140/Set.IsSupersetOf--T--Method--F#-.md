---
title: "Set.IsSupersetOf&lt;&#39;T&gt; Method (F#)"
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
  - Set.IsSupersetOf<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 07974083-5980-4f70-bad8-52b4a287b9ee
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.IsSupersetOf&lt;&#39;T&gt; Method (F#)
Evaluates to `true` if all elements of the second set are in the first.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.IsSupersetOf : Set<'T> -> bool (requires comparison)  
  
// Usage:  
set.IsSupersetOf (otherSet)  
```  
  
#### Parameters  
 `otherSet`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The set to test against.  
  
## Return Value  
 `true` if this set is a superset of `otherSet`.  
  
## Remarks  
  
## Example  
 The following code illustrates the use of the `IsSupersetOf` method.  
  
 [!CODE [FsSets#12](../CodeSnippet/VS_Snippets_Fsharp/fssets#12)]  
  
 **Output**  
  
 **set [1; 2; 3; 4; 5; 6; 7; 8; 9] is a superset of set [1; 2; 3; 4; 5; 6]: trueset [1; 2; 3; 4; 5; 6] is a superset of set [1; 2; 3; 4; 5; 6]: trueset [5; 6; 7; 8; 9; 10] is a superset of set [1; 2; 3; 4; 5; 6]: false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set<'T> Class (F#)](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)