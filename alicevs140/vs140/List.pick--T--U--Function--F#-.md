---
title: "List.pick&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - List.pick<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 0430b515-7fe4-49a1-a616-d2286d8b08b2
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.pick&lt;&#39;T,&#39;U&gt; Function (F#)
Applies the given function to successive elements, returning the first result where function returns `Some` for some value. If no such element exists then this function raises <xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.pick : ('T -> 'U option) -> 'T list -> 'U  
  
// Usage:  
List.pick chooser list  
```  
  
#### Parameters  
 `chooser`  
 Type: `'T -> 'U`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The function to generate options from the elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.Collections.Generic.KeyNotFoundException?qualifyHint=False>|Thrown when a matching element is not found or when the list is empty.|  
  
## Return Value  
 The first resulting value where `Some` is returned.  
  
## Remarks  
 This function is named `Pick` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `List.pick`.  
  
 [!CODE [FsLists#9](../CodeSnippet/VS_Snippets_Fsharp/fslists#9)]  
  
 **Output**  
  
 **"b"**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)