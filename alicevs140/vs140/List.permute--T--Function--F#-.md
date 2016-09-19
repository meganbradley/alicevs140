---
title: "List.permute&lt;&#39;T&gt; Function (F#)"
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
  - List.permute<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3de0d1b5-9526-4fc9-a4ed-5479d08009b8
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.permute&lt;&#39;T&gt; Function (F#)
Returns a list with all elements permuted according to the specified permutation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.permute : (int -> int) -> 'T list -> 'T list  
  
// Usage:  
List.permute indexMap list  
```  
  
#### Parameters  
 `indexMap`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `->`[int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The function to map input indices to output indices.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The permuted list.  
  
## Remarks  
 This function is named `Permute` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code demonstrates how to use `List.permute`.  
  
 [!CODE [FsLists#51](../CodeSnippet/VS_Snippets_Fsharp/fslists#51)]  
  
 **Output**  
  
 **[1; 2; 3; 4; 5]**  
**[5; 1; 2; 3; 4]**  
**[4; 5; 1; 2; 3]**  
**[3; 4; 5; 1; 2]**  
**[2; 3; 4; 5; 1]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)