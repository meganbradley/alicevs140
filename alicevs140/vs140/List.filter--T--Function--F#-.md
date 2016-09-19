---
title: "List.filter&lt;&#39;T&gt; Function (F#)"
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
  - List.filter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 11a8c926-547b-44dd-bbae-98d44f3dd248
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.filter&lt;&#39;T&gt; Function (F#)
Returns a new collection containing only the elements of the collection for which the given predicate returns `true`.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.filter : ('T -> bool) -> 'T list -> 'T list  
  
// Usage:  
List.filter predicate list  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 A list containing only the elements that satisfy the predicate.  
  
## Remarks  
 This function is named `Filter` in compiled assembly. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `List.filter`.  
  
 [!CODE [FsLists#24](../CodeSnippet/VS_Snippets_Fsharp/fslists#24)]  
  
 The resulting list is [2; 4; 6].  
  
## Example  
 The following example shows another typical use for `List.filter`.  
  
 [!CODE [FsSamples101#3007](../CodeSnippet/VS_Snippets_Fsharp/fssamples101#3007)]  
  
 **Animals with short names: [("Cats", 4); ("Dogs", 5); ("Mice", 3)]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)