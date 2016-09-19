---
title: "List.ofSeq&lt;&#39;T&gt; Function (F#)"
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
  - List.of_seq<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 74ab9289-4a59-4433-92eb-3f662d7f7db0
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.ofSeq&lt;&#39;T&gt; Function (F#)
Creates a new list from the given enumerable object.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.ofSeq : seq<'T> -> 'T list  
  
// Usage:  
List.ofSeq source  
```  
  
#### Parameters  
 `source`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T>`  
  
 The input sequence.  
  
## Return Value  
 The list of elements from the sequence.  
  
## Remarks  
 This function is named `OfSeq` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.ofSeq`.  
  
 [!CODE [FsLists#60](../CodeSnippet/VS_Snippets_Fsharp/fslists#60)]  
  
 **F# Interactive Output**  
  
 **val list1 : int list = [1; 2; 3; 4; 5; 6; 7; 8; 9; 10]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)