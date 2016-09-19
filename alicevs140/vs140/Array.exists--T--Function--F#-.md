---
title: "Array.exists&lt;&#39;T&gt; Function (F#)"
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
  - Array.exists<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8e47ad6c-c065-4876-8cb4-ec960ec3e5c9
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.exists&lt;&#39;T&gt; Function (F#)
Tests if any element of the array satisfies the given predicate.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.exists : ('T -> bool) -> 'T [] -> bool  
  
// Usage:  
Array.exists predicate array  
```  
  
#### Parameters  
 `predicate`  
 Type: `'T ->`[bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The function to test the input elements.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 `true` if any result from `predicate` is `true`. Otherwise, `false`.  
  
## Remarks  
 The predicate is applied to the elements of the input array. If any application returns `true` then the overall result is `true` and no further elements are tested.  
  
 This function is named `Exists` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates how to test the elements of an array by using `Array.exists`.  
  
 [!CODE [FsArrays#231](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#231)]  
  
 **true**  
**false**  
**false**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)