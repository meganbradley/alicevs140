---
title: "Array.sum&lt;^T&gt; Function (F#)"
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
  - Array.sum<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 4ffdb8c8-cd94-4b0b-9e5c-a7c9c17963c2
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.sum&lt;^T&gt; Function (F#)
Returns the sum of the elements in the array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.sum : ^T [] -> ^T (requires ^T with static member (+) and ^T with static member Zero)  
  
// Usage:  
Array.sum array  
```  
  
#### Parameters  
 `array`  
 Type: `^T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The resulting sum.  
  
## Remarks  
 This function is named `Sum` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Array.sum`.  
  
 [!CODE [FsArrays#66](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#66)]  
  
 **Output**  
  
 **55**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)