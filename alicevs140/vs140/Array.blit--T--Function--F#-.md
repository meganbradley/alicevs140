---
title: "Array.blit&lt;&#39;T&gt; Function (F#)"
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
  - Array.blit<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 675e13e4-7fb9-4e0d-a5be-a112830de667
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.blit&lt;&#39;T&gt; Function (F#)
Reads a range of elements from the first array and writes them into the second.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.blit : 'T [] -> int -> 'T [] -> int -> int -> unit  
  
// Usage:  
Array.blit source sourceIndex target targetIndex count  
```  
  
#### Parameters  
 `source`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The source array.  
  
 `sourceIndex`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The starting index of the source array.  
  
 `target`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The target array.  
  
 `targetIndex`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The starting index of the target array.  
  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements to copy.  
  
## Remarks  
 This function is named `CopyTo` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example illustrates the use of `Array.blit`.  
  
 [!CODE [FsArrays#30](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#30)]  
  
 **Output**  
  
 **[&#124;0; 0; 0; 0; 0; 4; 5; 6; 7; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0; 0&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)