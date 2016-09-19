---
title: "Set.( - )&lt;&#39;T&gt; Method (F#)"
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
  - Set.( - )<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 25274a0f-01e0-4e11-8ca0-42f664cb5405
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.( - )&lt;&#39;T&gt; Method (F#)
Returns a new set with the elements of the second set removed from the first.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member ( - ) : Set<'T> * Set<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
set1 - set2  
```  
  
#### Parameters  
 `set1`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The first input set.  
  
 `set2`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The second input set.  
  
## Return Value  
 A set containing elements of the first set that are not contained in the second set.  
  
## Remarks  
  
## Example  
 The following code illustrates the use of the + and - operators on sets.  
  
 [!CODE [FsSets#1](../CodeSnippet/VS_Snippets_Fsharp/fssets#1)]  
  
 **Output**  
  
 **set1: set [1; 2; 3]set2: set [4; 5; 6]set3 = set1 + set2: set [1; 2; 3; 4; 5; 6]set3 - set1: set [4; 5; 6]set3 - set2: set [1; 2; 3]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set<'T> Class (F#)](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)