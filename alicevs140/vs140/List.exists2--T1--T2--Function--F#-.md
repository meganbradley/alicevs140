---
title: "List.exists2&lt;&#39;T1,&#39;T2&gt; Function (F#)"
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
  - List.exists2<'T1,'T2>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7532b39e-3f4f-4534-a60b-d7721dc6fa7e
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.exists2&lt;&#39;T1,&#39;T2&gt; Function (F#)
Tests if any pair of corresponding elements of the lists satisfies the given predicate.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.exists2 : ('T1 -> 'T2 -> bool) -> 'T1 list -> 'T2 list -> bool  
  
// Usage:  
List.exists2 predicate list1 list2  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T1 -> 'T2 ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `list1`  
 Type: `'T1`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The first input list.  
  
 `list2`  
 Type: `'T2`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The second input list.  
  
## Return Value  
 `true` if any pair of elements satisfy the predicate. Otherwise, returns `false`.  
  
## Remarks  
 The predicate is applied to matching elements in the two collections up to the lesser of the two lengths of the collections. If any application returns true then the overall result is true and no further elements are tested.  
  
 This function is named `Exists2` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.exists2`.  
  
 [!CODE [FsLists#2](../CodeSnippet/VS_Snippets_Fsharp/fslists#2)]  
  
 **Output**  
  
 **Lists [1; 2; 3; 4; 5] and [5; 4; 3; 2; 1] have at least one equal element at the same position.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)