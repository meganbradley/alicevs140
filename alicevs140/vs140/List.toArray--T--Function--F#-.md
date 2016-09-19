---
title: "List.toArray&lt;&#39;T&gt; Function (F#)"
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
  - List.to_array<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ac87dd82-a0cd-40b3-b1fa-dd3168134547
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.toArray&lt;&#39;T&gt; Function (F#)
Creates an array from the given list.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.toArray : 'T list -> 'T []  
  
// Usage:  
List.toArray list  
```  
  
#### Parameters  
 `list`  
 Type: `'T` [list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The array containing the elements of the list.  
  
## Remarks  
 This function is named `ToArray` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.toArray`.  
  
 [!CODE [FsLists#64](../CodeSnippet/VS_Snippets_Fsharp/fslists#64)]  
  
 **Output**  
  
 **[&#124;-10; -2; 1; 3&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)