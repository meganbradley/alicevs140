---
title: "List.tail&lt;&#39;T&gt; Function (F#)"
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
  - List.tl<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: da0a0638-4420-4571-84b6-d09ae601f601
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.tail&lt;&#39;T&gt; Function (F#)
Returns the list without the first element.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.tail : 'T list -> 'T list  
  
// Usage:  
List.tail list  
```  
  
#### Parameters  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
## Return Value  
 The tail of the list, that is, the list without the first element.  
  
## Remarks  
 This function is named `Tail` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.tail`.  
  
 [!CODE [FsLists#63](../CodeSnippet/VS_Snippets_Fsharp/fslists#63)]  
  
 **Abbreviated Output**  
  
 **[2; 3]System.ArgumentException: The input list was empty.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)