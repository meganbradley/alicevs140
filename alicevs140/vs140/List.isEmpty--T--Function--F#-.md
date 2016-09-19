---
title: "List.isEmpty&lt;&#39;T&gt; Function (F#)"
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
  - List.isEmpty<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a7941d44-9e92-427c-b806-c378f4558107
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.isEmpty&lt;&#39;T&gt; Function (F#)
Tests whether a list is empty.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.isEmpty : 'T list -> bool  
  
// Usage:  
List.isEmpty list  
```  
  
#### Parameters  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 `true` if the list is empty. Otherwise, returns `false`.  
  
## Remarks  
 This function is named `IsEmpty` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.isEmpty`.  
  
 [!CODE [FsLists#47](../CodeSnippet/VS_Snippets_Fsharp/fslists#47)]  
  
 **Output**  
  
 **This list contains the following elements:**  
**"test1" "test2"**   
**There are no elements in this list.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)