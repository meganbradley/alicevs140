---
title: "Array.toList&lt;&#39;T&gt; Function (F#)"
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
  - Array.to_list<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 4deff724-0be4-4688-92e7-9d67a1097786
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.toList&lt;&#39;T&gt; Function (F#)
Builds a list from the given array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.toList : 'T [] -> 'T list  
  
// Usage:  
Array.toList array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The list of array elements.  
  
## Remarks  
 This function is named `ToList` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example shows how to use `Array.toList`.  
  
 [!CODE [FsArrays#68](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#68)]  
  
 **Output**  
  
 **10 9 8 7 6 5 4 3 2 1**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)