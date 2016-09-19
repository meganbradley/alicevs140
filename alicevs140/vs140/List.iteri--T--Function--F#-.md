---
title: "List.iteri&lt;&#39;T&gt; Function (F#)"
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
  - List.iteri<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 6dd21ae6-5c00-41cd-8306-821e513d8f60
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.iteri&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the collection. The integer passed to the function indicates the index of element.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.List  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.iteri : (int -> 'T -> unit) -> 'T list -> unit  
  
// Usage:  
List.iteri action list  
```  
  
#### Parameters  
 `action`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T ->`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to apply to the elements of the list along with their index.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Remarks  
 This function is named `IterateIndexed` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `List.iteri`.  
  
 [!CODE [FsSamples101#3005](../CodeSnippet/VS_Snippets_Fsharp/fssamples101#3005)]  
  
 **item 0: Cats**  
**item 1: Dogs**  
**item 2: Mice**  
**item 3: Elephants**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)