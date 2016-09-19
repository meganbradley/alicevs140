---
title: "Array.filter&lt;&#39;T&gt; Function (F#)"
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
  - Array.filter<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b885b214-47fc-4639-9664-b8c183a39ede
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.filter&lt;&#39;T&gt; Function (F#)
Returns a new collection containing only the elements of the collection for which the given predicate returns `true`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.filter : ('T -> bool) -> 'T [] -> 'T []  
  
// Usage:  
Array.filter predicate array  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 An array containing the elements for which the given predicate returns `true`.  
  
## Remarks  
 This function is named `Filter` in compiled assemblies. If accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example shows how to use `Array.filter` to select elements from an array.  
  
 [!CODE [FsSamples101#1007](../CodeSnippet/VS_Snippets_Fsharp/fssamples101#1007)]  
  
 **names = [&#124;"Bob"; "Ann"; "Stephen"; "Vivek"; "Fred"; "Kim"; "Brian"; "Ling"; "Jane"; "Jonathan"&#124;]**  
**longNames = [&#124;"Stephen"; "Vivek"; "Brian"; "Jonathan"&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)