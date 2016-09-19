---
title: "List.tryFind&lt;&#39;T&gt; Function (F#)"
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
  - List.tryFind<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 37f4532e-9fd0-4802-8bbd-e1aa2380287d
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.tryFind&lt;&#39;T&gt; Function (F#)
Returns the first element for which the given function returns `true``.` Returns `None` if no such element exists.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.tryFind : ('T -> bool) -> 'T list -> 'T option  
  
// Usage:  
List.tryFind predicate list  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The first element for which the predicate returns true, or None if every element evaluates to false.  
  
## Remarks  
 This function is named `TryFind` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.tryFind` and `List.tryFindIndex`.  
  
 [!CODE [FsLists#10](../CodeSnippet/VS_Snippets_Fsharp/fslists#10)]  
  
 **Output**  
  
 **The first even value is 22.**  
**The first even value is at position 8.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)