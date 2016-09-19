---
title: "Array.unzip&lt;&#39;T1,&#39;T2&gt; Function (F#)"
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
  - Array.unzip<'T1,'T2>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a529b47c-2e2b-4f79-ad44-c578432d2f48
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.unzip&lt;&#39;T1,&#39;T2&gt; Function (F#)
Splits an array of pairs into two arrays.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.unzip : ('T1 * 'T2) [] -> 'T1 [] * 'T2 []  
  
// Usage:  
Array.unzip array  
```  
  
#### Parameters  
 `array`  
 Type: `('T1 * 'T2)`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The two arrays.  
  
## Remarks  
 This function is named `Unzip` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Array.unzip`.  
  
 [!CODE [FsArrays#70](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#70)]  
  
 **Output**  
  
 **[&#124;1; 3&#124;]**  
**[&#124;2; 4&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)