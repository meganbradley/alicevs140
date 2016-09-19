---
title: "Array.toSeq&lt;&#39;T&gt; Function (F#)"
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
  - Array.to_seq<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ac28dbab-406c-4fe0-ab08-c1ce5e247af4
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.toSeq&lt;&#39;T&gt; Function (F#)
Views the given array as a sequence.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.toSeq : 'T [] -> seq<'T>  
  
// Usage:  
Array.toSeq array  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The sequence of array elements.  
  
## Remarks  
 This function is named `ToSeq` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Array.toSeq`.  
  
 [!CODE [FsArrays#69](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#69)]  
  
 **Output**  
  
 **1 2 3 4 5**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)