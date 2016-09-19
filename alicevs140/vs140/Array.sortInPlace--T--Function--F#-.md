---
title: "Array.sortInPlace&lt;&#39;T&gt; Function (F#)"
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
  - Array.sortInPlace<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 36f39947-8a88-4823-9e9b-e9d838d292e0
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.sortInPlace&lt;&#39;T&gt; Function (F#)
Sorts the elements of an array by mutating the array in-place, using the given comparison function. Elements are compared using [Operators.compare](../vs140/Operators.compare--T--Function--F#-.md).  
  
 **Namespace/Module Path**: Microsoft.FSharp.Collections.Array  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.sortInPlace : 'T [] -> unit (requires comparison)  
  
// Usage:  
Array.sortInPlace array  
```  
  
#### Parameters  
 `array`  
 Type: `'T` [&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Remarks  
 This function is named `SortInPlace` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.sortInPlace`.  
  
 [!CODE [FsArrays#40](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#40)]  
  
 **Output**  
  
 **[&#124;-2; 1; 4; 5; 8&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)