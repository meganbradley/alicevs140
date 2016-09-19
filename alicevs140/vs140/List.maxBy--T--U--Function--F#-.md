---
title: "List.maxBy&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - List.maxBy<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 75a75ef0-9bba-4078-8e77-f468f5679e1e
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.maxBy&lt;&#39;T,&#39;U&gt; Function (F#)
Returns the greatest of all elements of the list, compared by using [Operators.max](../vs140/Operators.max--T--Function--F#-.md) on the function result.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.maxBy : ('T -> 'U) -> 'T list -> 'T (requires comparison)  
  
// Usage:  
List.maxBy projection list  
```  
  
#### Parameters  
 `projection`  
 Type: `'T -> 'U`  
  
 The function to transform the list elements into the type to be compared.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the list is empty.|  
  
## Return Value  
 The maximum element.  
  
## Remarks  
 This function is named `MaxBy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `List.maxBy`.  
  
 [!CODE [FsLists#56](../CodeSnippet/VS_Snippets_Fsharp/fslists#56)]  
  
 **Output**  
  
 **0.0**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)