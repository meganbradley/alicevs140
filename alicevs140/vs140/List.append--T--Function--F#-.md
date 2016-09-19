---
title: "List.append&lt;&#39;T&gt; Function (F#)"
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
  - List.append<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2954da80-3f4a-4a4b-9371-794645c03426
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.append&lt;&#39;T&gt; Function (F#)
Returns a new list that contains the elements of the first list followed by elements of the second.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.append : 'T list -> 'T list -> 'T list  
  
// Usage:  
List.append list1 list2  
```  
  
#### Parameters  
 `list1`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The first input list.  
  
 `list2`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The second input list.  
  
## Return Value  
 The resulting list.  
  
## Remarks  
 This function is named `Append` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.append` to join two lists together. Use [List.concat](../vs140/List.concat--T--Function--F#-.md) to join more than two lists.  
  
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