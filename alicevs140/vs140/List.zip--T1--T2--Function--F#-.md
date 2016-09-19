---
title: "List.zip&lt;&#39;T1,&#39;T2&gt; Function (F#)"
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
  - List.zip<'T1,'T2>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3028d790-8f48-4c94-bf08-b058bec3689c
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.zip&lt;&#39;T1,&#39;T2&gt; Function (F#)
Combines the two lists into a list of pairs. The two lists must have equal lengths.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.zip : 'T1 list -> 'T2 list -> ('T1 * 'T2) list  
  
// Usage:  
List.zip list1 list2  
```  
  
#### Parameters  
 `list1`  
 Type: `'T1`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The first input list.  
  
 `list2`  
 Type: `'T2`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The second input list.  
  
## Return Value  
 A single list containing pairs of matching elements from the input lists.  
  
## Remarks  
 This function is named `Zip` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.zip`.  
  
 [!CODE [FsLists#13](../CodeSnippet/VS_Snippets_Fsharp/fslists#13)]  
  
 **Output**  
  
 **[(1, -1); (2, -2); (3; -3)]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)