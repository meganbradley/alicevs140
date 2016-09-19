---
title: "Array.collect&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Array.collect<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c3b60c3b-9455-48c9-bc2b-e88f0434342a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.collect&lt;&#39;T,&#39;U&gt; Function (F#)
For each element of the array, applies the given function. Concatenates all the results and return the combined array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.collect : ('T -> 'U []) -> 'T [] -> 'U []  
  
// Usage:  
Array.collect mapping array  
```  
  
#### Parameters  
 `mapping`  
 Type: `'T -> 'U`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The function to create sub-arrays from the input array elements.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The concatenation of the subarrays.  
  
## Example  
 The following code demonstrates the use of `Array.collect` to concatenate subarrays that are generated from each array element.  
  
 [!CODE [FsArrays#15](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#15)]  
  
 **[&#124;0; 1; 0; 1; 2; 3; 4; 5; 0; 1; 2; 3; 4; 5; 6; 7; 8; 9; 10&#124;]**   
## Remarks  
 This function is named `Collect` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)