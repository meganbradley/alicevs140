---
title: "List.choose&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - List.choose<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2e21d3fb-ce35-4824-8a57-c4404616093d
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List.choose&lt;&#39;T,&#39;U&gt; Function (F#)
Applies the given function `f` to each element `x` of the list. Returns the list comprised of the results for each element where the function returns `Some(f(x))`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.List  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
List.choose : ('T -> 'U option) -> 'T list -> 'U list  
  
// Usage:  
List.choose chooser list  
```  
  
#### Parameters  
 `chooser`  
 Type: `'T -> 'U`[option](../vs140/Core.Option--T--Union--F#-.md)  
  
 The function to generate options from the elements.  
  
 `list`  
 Type: `'T`[list](../vs140/Collections.List--T--Union--F#-.md)  
  
 The input list.  
  
## Return Value  
 The list comprising the values selected from the chooser function.  
  
## Remarks  
 This function is named `Choose` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code demonstrates the use of `List.choose` to select capitalized words out of a list of words.  
  
 [!CODE [FsLists#25](../CodeSnippet/VS_Snippets_Fsharp/fslists#25)]  
  
 **Output**  
  
 **["Rome's"; "Bob's"]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.List Module (F#)](../vs140/Collections.List-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)