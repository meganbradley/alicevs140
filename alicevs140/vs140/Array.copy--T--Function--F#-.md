---
title: "Array.copy&lt;&#39;T&gt; Function (F#)"
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
  - Array.copy<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9d0202f1-1ea0-475e-9d66-4f8ccc3c5b5f
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.copy&lt;&#39;T&gt; Function (F#)
Builds a new array that contains the elements of the given array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.copy : 'T [] -> 'T []  
  
// Usage:  
Array.copy array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 A copy of the input array.  
  
## Remarks  
 This function is named `Copy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.copy`.  
  
 [!CODE [FsArrays#31](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#31)]  
  
 **Output**  
  
 **[&#124;1; 2; 3; 4; 5; 6; 7; 8; 9; 10&#124;]**  
**[&#124;1; 2; 3; 4; 5; 6; 7; 8; 9; 10&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)