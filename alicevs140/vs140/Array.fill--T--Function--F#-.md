---
title: "Array.fill&lt;&#39;T&gt; Function (F#)"
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
  - Array.fill<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c83c9886-81d9-44f9-a195-61c7b87f7df2
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.fill&lt;&#39;T&gt; Function (F#)
Fills a range of elements of the array with the given value.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.fill : 'T [] -> int -> int -> 'T -> unit  
  
// Usage:  
Array.fill target targetIndex count value  
```  
  
#### Parameters  
 `target`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The target array.  
  
 `targetIndex`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index of the first element to set.  
  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements to set.  
  
 `value`  
 Type: `'T`  
  
 The value to set.  
  
## Remarks  
 This function is named `Fill` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Array.fill` to overwrite a section of an array with zeroes.  
  
 [!CODE [FsArrays#28](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#28)]  
  
 **[&#124;1; 2; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 23; 24; 25&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)