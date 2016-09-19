---
title: "List.replicate&lt;&#39;T&gt; Function (F#)"
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
  - List.replicate<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 93647552-6e6f-41d4-8bb4-64c975ff94d1
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.replicate&lt;&#39;T&gt; Function (F#)
Creates a list of a specified length with every element set to the given value.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.replicate : int -> 'T -> 'T list  
  
// Usage:  
List.replicate count initial  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements to replicate.  
  
 `initial`  
 Type: `'T`  
  
 The value to replicate  
  
## Return Value  
 The generated list.  
  
## Remarks  
 This function is named `Replicate` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.replicate`.  
  
 [!CODE [FsLists#52](../CodeSnippet/VS_Snippets_Fsharp/fslists#52)]  
  
 **Output**  
  
 **["test"; "test"; "test"; "test"]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)