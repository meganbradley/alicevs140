---
title: "Set.intersect&lt;&#39;T&gt; Function (F#)"
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
  - Set.intersect<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 540f4b96-34d6-47f0-8881-e3a434abade1
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.intersect&lt;&#39;T&gt; Function (F#)
Computes the intersection of the two sets.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.intersect : Set<'T> -> Set<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.intersect set1 set2  
```  
  
#### Parameters  
 `set1`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The first input set.  
  
 `set2`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The second input set.  
  
## Return Value  
 The intersection of `set1` and `set2`.  
  
## Remarks  
 This function is named `Intersect` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of the `Set.intersect` function.  
  
 [!CODE [FsSets#4](../CodeSnippet/VS_Snippets_Fsharp/fssets#4)]  
  
 **Output**  
  
 **Set.intersect [1 .. 3] [2 .. 6] yields set [2; 3]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)