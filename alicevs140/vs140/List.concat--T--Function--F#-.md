---
title: "List.concat&lt;&#39;T&gt; Function (F#)"
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
  - List.concat<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c5afd433-8764-4ea8-a6a8-937fb4d77c4c
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.concat&lt;&#39;T&gt; Function (F#)
Returns a new list that contains the elements of each list in order.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.concat : seq<'T list> -> 'T list  
  
// Usage:  
List.concat lists  
```  
  
#### Parameters  
 `lists`  
 Type: [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)`<'T list>`  
  
 The input sequence of lists.  
  
## Return Value  
 The resulting concatenated list.  
  
## Remarks  
 This function is named `Concat` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates that [List.append](../vs140/List.append--T--Function--F#-.md) is used to join two lists together; and `List.concat` is used to join any number of lists.  
  
 [!CODE [FsLists#26](../CodeSnippet/VS_Snippets_Fsharp/fslists#26)]  
  
 **Output**  
  
 **1 2 3 4 5 6 7 8 9 10**   
**1 2 3 4 5 6 7 8 9**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)