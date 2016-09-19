---
title: "Array.unzip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)"
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
  - Array.unzip3<'T1,'T2,'T3>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: bc3e6db0-f334-444f-8c30-813942880677
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.unzip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)
Splits an array of triples into three arrays.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.unzip3 : ('T1 * 'T2 * 'T3) [] -> 'T1 [] * 'T2 [] * 'T3 []  
  
// Usage:  
Array.unzip3 array  
```  
  
#### Parameters  
 `array`  
 Type: `('T1 * 'T2 * 'T3)`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Return Value  
 The tuple of three arrays.  
  
## Remarks  
 This function is named `Unzip3` in compiled assemblies. If accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use Array.unzip3.  
  
 [!CODE [FsArrays#71](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#71)]  
  
 **Output**  
  
 **[&#124;1; 3&#124;]**  
**[&#124;2; 4&#124;]**  
**[&#124;3; 5&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)