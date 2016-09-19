---
title: "List.sortWith&lt;&#39;T&gt; Function (F#)"
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
  - List.sortWith<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1d806a54-9166-4198-906d-15101f7916c7
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.sortWith&lt;&#39;T&gt; Function (F#)
Sorts the given list using the given comparison function.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.sortWith : ('T -> 'T -> int) -> 'T list -> 'T list  
  
// Usage:  
List.sortWith comparer list  
```  
  
#### Parameters  
 `comparer`  
 Type: `'T -> 'T ->`[int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The function to compare the list elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The sorted list.  
  
## Remarks  
 This is a stable sort, that is, the original order of equal elements is preserved.  
  
 This function is named `SortWith` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.sortWith`.  
  
 [!CODE [FsLists#62](../CodeSnippet/VS_Snippets_Fsharp/fslists#62)]  
  
 **Output**  
  
 **Before sorting:**   
**["<>"; "&"; "&&"; "&&&"; "<"; ">"; "&#124;"; "&#124;&#124;"; "&#124;&#124;&#124;"]**  
**After sorting:**  
**["&"; "&#124;"; "<"; ">"; "&&"; "&#124;&#124;"; "<>"; "&&&"; "&#124;&#124;&#124;"]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)