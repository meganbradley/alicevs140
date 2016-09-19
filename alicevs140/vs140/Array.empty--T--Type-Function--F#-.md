---
title: "Array.empty&lt;&#39;T&gt; Type Function (F#)"
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
  - Array.empty<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c3694b92-1c16-4c54-9bf2-fe398fadce32
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.empty&lt;&#39;T&gt; Type Function (F#)
Returns an empty array of the given type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.empty<'T> :  'T []  
  
// Usage:  
Array.empty  
```  
  
## Return Value  
 An empty array.  
  
## Remarks  
 This function is named `Empty` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Array.empty`.  
  
 [!CODE [FsArrays#44](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#44)]  
  
 **Output**  
  
 **Length of empty array: 0**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)