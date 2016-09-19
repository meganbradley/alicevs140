---
title: "List.exists&lt;&#39;T&gt; Function (F#)"
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
  - List.exists<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 15a3ebd5-98f0-44c0-8220-7dedec3e68a8
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.exists&lt;&#39;T&gt; Function (F#)
Tests if any element of the list satisfies the given predicate.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.exists : ('T -> bool) -> 'T list -> bool  
  
// Usage:  
List.exists predicate list  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 `true` if any element satisfies the predicate. Otherwise, returns `false`.  
  
## Remarks  
 The predicate is applied to the elements of the input list. If any application returns `true` then the overall result is `true` and no further elements are tested.  
  
 This function is named `Exists` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `List.exists` to determine whether a given element exists in a list.  
  
 [!CODE [FsLists#1](../CodeSnippet/VS_Snippets_Fsharp/fslists#1)]  
  
 **Output**  
  
 **For list [0; 1; 2; 3], contains zero is true**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)