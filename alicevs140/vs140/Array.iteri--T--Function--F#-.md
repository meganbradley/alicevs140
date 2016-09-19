---
title: "Array.iteri&lt;&#39;T&gt; Function (F#)"
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
  - Array.iteri<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8bbe2ed4-ada7-4906-ac3e-cb09f9db6486
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.iteri&lt;&#39;T&gt; Function (F#)
Applies the given function to each element of the array. The integer passed to the function indicates the index of element.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.iteri : (int -> 'T -> unit) -> 'T [] -> unit  
  
// Usage:  
Array.iteri action array  
```  
  
#### Parameters  
 `action`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md) `-> 'T ->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)  
  
 The function to apply to each index and element.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Remarks  
 This function is named `IterateIndexed` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code examples shows the differences between [Array.iter](../vs140/Array.iter--T--Function--F#-.md), [Array.iter2](../Topic/Array.iter2%3C'T1,'T2%3E%20Function%20\(F%23\).md), `Array.iteri`, and [Array.iteri2](../Topic/Array.iteri2%3C'T1,'T2%3E%20Function%20\(F%23\).md).  
  
 [!CODE [FsArrays#49](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#49)]  
  
 **Output**  
  
 **Array.iter: element is 1**  
**Array.iter: element is 2**  
**Array.iter: element is 3**  
**Array.iteri: element 0 is 1**  
**Array.iteri: element 1 is 2**  
**Array.iteri: element 2 is 3**  
**Array.iter2: elements are 1 4**  
**Array.iter2: elements are 2 5**  
**Array.iter2: elements are 3 6**  
**Array.iteri2: element 0 of array1 is 1 element 0 of array2 is 4**  
**Array.iteri2: element 1 of array1 is 2 element 1 of array2 is 5**  
**Array.iteri2: element 2 of array1 is 3 element 2 of array2 is 6**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)