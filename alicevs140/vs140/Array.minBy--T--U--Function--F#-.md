---
title: "Array.minBy&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Array.minBy<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 24091583-be78-4cc9-9fab-de6d7506af4f
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array.minBy&lt;&#39;T,&#39;U&gt; Function (F#)
Returns the lowest of all elements of the array, compared by using [Operators.min](../vs140/Operators.min--T--Function--F#-.md) on the function result.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array.minBy : ('T -> 'U) -> 'T [] -> 'T (requires comparison)  
  
// Usage:  
Array.minBy projection array  
```  
  
#### Parameters  
 `projection`  
 Type: `'T -> 'U`  
  
 The function to transform the elements into a type supporting comparison.  
  
 `array`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The input array.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input array is empty.|  
  
## Return Value  
 The minimum element.  
  
## Remarks  
 This function is named `MinBy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Example  
 The following code example demonstrates the use of `Array.minBy`.  
  
 [!CODE [FsArrays#58](../CodeSnippet/VS_Snippets_Fsharp/fsarrays#58)]  
  
 **Output**  
  
 **0.0**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array Module (F#)](../Topic/Collections.Array%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)