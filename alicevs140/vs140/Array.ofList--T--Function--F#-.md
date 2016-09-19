---
title: "Array.ofList&lt;&#39;T&gt; Function (F#)"
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
  - Array.of_list<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e7225239-f561-45a4-b0b5-69a1cdcae78b
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.ofList&lt;&#39;T&gt; Function (F#)
Builds an array from the given list.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.ofList : 'T list -> 'T []  
  
// Usage:  
Array.ofList list  
```  
  
#### Parameters  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The array of elements from the list.  
  
## Remarks  
 This function is named `OfList` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example demonstrates the use of `Array.ofList`.  
  
 [!CODE [FsArrays#59](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#59)]  
  
 **FSI Output**  
  
 **val array1 : int [] = [&#124;1; 2; 3; 4; 5; 6; 7; 8; 9; 10&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)