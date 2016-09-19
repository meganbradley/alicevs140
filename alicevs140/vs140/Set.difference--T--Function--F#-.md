---
title: "Set.difference&lt;&#39;T&gt; Function (F#)"
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
  - Set.difference<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 75bf5d03-8825-4b21-8526-4da87ea419e6
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.difference&lt;&#39;T&gt; Function (F#)
Returns a new set with the elements of the second set removed from the first.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.difference : Set<'T> -> Set<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.difference set1 set2  
```  
  
#### Parameters  
 `set1`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The first input set.  
  
 `set2`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The set whose elements will be removed from `set1`.  
  
## Return Value  
 The set with the elements of `set2` removed from `set1`.  
  
## Remarks  
 This function is named `Difference` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of the `Set.difference` function.  
  
 [!CODE [FsSets#2](../CodeSnippet/VS_Snippets_Fsharp/fssets#2)]  
  
 **Output**  
  
 **Set.difference [2 .. 6] [1 .. 3] yields set [4; 5; 6]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)