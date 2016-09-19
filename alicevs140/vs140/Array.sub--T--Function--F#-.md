---
title: "Array.sub&lt;&#39;T&gt; Function (F#)"
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
  - Array.sub<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 40fb12ba-41d7-4ef0-b33a-56727deeef9d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.sub&lt;&#39;T&gt; Function (F#)
Builds a new array that contains the given subrange specified by starting index and length.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.sub : 'T [] -> int -> int -> 'T []  
  
// Usage:  
Array.sub array startIndex count  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
 `startIndex`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index of the first element of the subarray.  
  
 `count`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The length of the subarray.  
  
## Return Value  
 The created subarray.  
  
## Remarks  
 This function is named `GetSubArray` in compiled assemblies. If accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following example shows the use of `Array.sub` to specify a subarray. The output shows that the subarray starts at a zero-based index of 5 and has 10 elements.  
  
 [!CODE [FsArrays#12](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#12)]  
  
 **[&#124;5; 6; 7; 8; 9; 10; 11; 12; 13; 14&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)