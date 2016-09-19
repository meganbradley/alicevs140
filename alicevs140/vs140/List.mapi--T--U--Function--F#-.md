---
title: "List.mapi&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - List.mapi<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 284b9234-3d26-409b-b328-ac79638d9e14
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.mapi&lt;&#39;T,&#39;U&gt; Function (F#)
Creates a new collection whose elements are the results of applying the given function to each of the elements of the collection. The integer index passed to the function indicates the index (from 0) of element being transformed.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.mapi : (int -> 'T -> 'U) -> 'T list -> 'U list  
  
// Usage:  
List.mapi mapping list  
```  
  
#### Parameters  
 `mapping`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T -> 'U`  
  
 The function to transform elements and their indices.  
  
 `list`  
 Type: `'T` [list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The list of transformed elements.  
  
## Remarks  
 This function is named `MapIndexed` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.mapi`.  
  
 [!CODE [FsLists#36](../CodeSnippet/VS_Snippets_Fsharp/fslists#36)]  
  
 **Output**  
  
 **[(0, 1); (1, 2); (2, 3)]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)