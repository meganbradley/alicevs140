---
title: "Array.sort&lt;&#39;T&gt; Function (F#)"
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
  - Array.sort<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c6679075-e7eb-463c-9be5-c89be140c312
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.sort&lt;&#39;T&gt; Function (F#)
Sorts the elements of an array, returning a new array. Elements are compared using [Operators.compare](../vs140/Operators.compare--T--Function--F#-.md).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.sort : 'T [] -> 'T [] (requires comparison)  
  
// Usage:  
Array.sort array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The sorted array.  
  
## Remarks  
 This is not a stable sort. Therefore, the original order of equal elements might not be preserved. For a stable sort, consider using [Seq.sort](../vs140/Seq.sort--T--Function--F#-.md).  
  
 This function is named `Sort` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code illustrates the use of `Array.sort`.  
  
 [!CODE [FsArrays#37](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#37)]  
  
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