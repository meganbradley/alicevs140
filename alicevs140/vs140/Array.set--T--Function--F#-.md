---
title: "Array.set&lt;&#39;T&gt; Function (F#)"
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
  - Array.set<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 847edc0d-4dc5-4a39-98c7-d4320c60e790
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.set&lt;&#39;T&gt; Function (F#)
Sets an element of an array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.set : 'T [] -> int -> 'T -> unit  
  
// Usage:  
Array.set array index value  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
 `index`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The input index.  
  
 `value`  
 Type: `'T`  
  
 The input value.  
  
## Remarks  
 This function is named `Set` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates creating, setting and getting array values.  
  
 [!CODE [FsArrays#9](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#9)]  
  
 **0 1 2 3 4 5 6 7 8 9**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)