---
title: "List.collect&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - List.collect<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: cd08bbc7-a3b9-40ab-8c20-4e85ec84664f
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.collect&lt;&#39;T,&#39;U&gt; Function (F#)
For each element of the list, applies the given function. Concatenates all the results and returns the combined list.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.collect : ('T -> 'U list) -> 'T list -> 'U list  
  
// Usage:  
List.collect mapping list  
```  
  
#### Parameters  
 `mapping`  
 Type: `'T -> 'U`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The function to transform each input element into a sublist to be concatenated.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The concatenation of the resulting sublists.  
  
## Remarks  
 This function is named `Collect` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.collect`.  
  
 [!CODE [FsLists#42](../CodeSnippet/VS_Snippets_Fsharp/fslists#42)]  
  
 **Output**  
  
 **[10; 20; 30; 20; 40; 60; 30; 60; 90]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)