---
title: "List.sortBy&lt;&#39;T,&#39;Key&gt; Function (F#)"
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
  - List.sortBy<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 955bfc5f-ad9c-4f2d-a7ab-91e43eb21359
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.sortBy&lt;&#39;T,&#39;Key&gt; Function (F#)
Sorts the given list using keys given by the given projection. Keys are compared using [Operators.compare](../vs140/Operators.compare--T--Function--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.sortBy : ('T -> 'Key) -> 'T list -> 'T list (requires comparison)  
  
// Usage:  
List.sortBy projection list  
```  
  
#### Parameters  
 `projection`  
 Type: `'T -> 'Key`  
  
 The function to transform the list elements into the type to be compared.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The sorted list.  
  
## Remarks  
 This is a stable sort, that is, the original order of equal elements is preserved.  
  
 This function is named `SortBy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.sortBy`.  
  
 [!CODE [FsLists#6](../CodeSnippet/VS_Snippets_Fsharp/fslists#6)]  
  
 **Output**  
  
 **[1; -2; 4; 5; 8]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)