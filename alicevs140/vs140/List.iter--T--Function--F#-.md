---
title: "List.iter&lt;&#39;T&gt; Function (F#)"
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
  - List.iter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f778d075-81a9-4994-af60-cddcc53a201f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.iter&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the collection.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.iter : ('T -> unit) -> 'T list -> unit  
  
// Usage:  
List.iter action list  
```  
  
#### Parameters  
 `action`  
 Type: `'T ->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to apply to elements from the input list.  
  
 `list`  
 Type: `'T` [list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Remarks  
 This function is named `Iterate` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `List.iter`.  
  
 [!CODE [FsSamples101#3004](../CodeSnippet/VS_Snippets_Fsharp/fssamples101#3004)]  
  
 **item: Cats**  
**item: Dogs**  
**item: Mice**  
**item: Elephants**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)