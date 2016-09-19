---
title: "Array.zip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)"
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
  - Array.zip3<'T1,'T2,'T3>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1745744a-d2ca-4c3e-b825-3f15d9f4000d
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.zip3&lt;&#39;T1,&#39;T2,&#39;T3&gt; Function (F#)
Combines three arrays into an array of tuples with three elements. The three arrays must have equal lengths, otherwise an <xref:System.ArgumentException?qualifyHint=False> is raised.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.zip3 : 'T1 [] -> 'T2 [] -> 'T3 [] -> ('T1 * 'T2 * 'T3) []  
  
// Usage:  
Array.zip3 array1 array2 array3  
```  
  
#### Parameters  
 `array1`  
 Type: `'T1`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The first input array.  
  
 `array2`  
 Type: `'T2`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The second input array.  
  
 `array3`  
 Type: `'T3`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The third input array.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input arrays differ in length.|  
  
## Return Value  
 The array of tupled elements.  
  
## Remarks  
 This function is named `Zip3` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code shows how to use `Array.zip3`.  
  
 [!CODE [FsArrays#73](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#73)]  
  
 **Output**  
  
 **[&#124;(1, -1, "horse"); (2, -2, "dog"); (3, -3, "elephant")&#124;]**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)