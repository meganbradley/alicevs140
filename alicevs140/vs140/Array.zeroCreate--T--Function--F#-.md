---
title: "Array.zeroCreate&lt;&#39;T&gt; Function (F#)"
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
  - Array.zeroCreate<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fa5b8e7a-1b5b-411c-8622-b58d7a14d3b2
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.zeroCreate&lt;&#39;T&gt; Function (F#)
Creates an array where the entries are initially the default value [Unchecked.defaultof<'T>](../vs140/Unchecked.defaultof--T--Type-Function--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.zeroCreate : int -> 'T []  
  
// Usage:  
Array.zeroCreate count  
```  
  
#### Parameters  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the array to create.  
  
## Return Value  
 The created array.  
  
## Remarks  
 This function is named `ZeroCreate` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example demonstrates the use of `Array.zeroCreate`.  
  
 [!CODE [FsArrays#4](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#4)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)