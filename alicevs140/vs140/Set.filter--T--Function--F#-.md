---
title: "Set.filter&lt;&#39;T&gt; Function (F#)"
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
  - Set.filter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 085960a3-1909-4ed1-985b-3f023dc4bd5f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set.filter&lt;&#39;T&gt; Function (F#)
Returns a new collection containing only the elements of the collection for which the given predicate returns `true`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Set  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Set.filter : ('T -> bool) -> Set<'T> -> Set<'T> (requires comparison)  
  
// Usage:  
Set.filter predicate set  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->` [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test set elements.  
  
 `set`  
 Type: [Set](../Topic/Collections.Set%3C'T%3E%20Class%20\(F%23\).md)`<'T>`  
  
 The input set.  
  
## Return Value  
 The set containing only the elements for which `predicate` returns `true`.  
  
## Remarks  
 This function is named `Filter` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of the `Set.filter` function.  
  
 [!CODE [FsSets#3](../CodeSnippet/VS_Snippets_Fsharp/fssets#3)]  
  
 **Output**  
  
 **set [2; 4; 6; 8; 10]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Set Module (F#)](../vs140/Collections.Set-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)