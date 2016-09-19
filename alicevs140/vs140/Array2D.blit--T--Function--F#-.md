---
title: "Array2D.blit&lt;&#39;T&gt; Function (F#)"
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
  - Array2D.blit<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c1f7709d-3276-4e5f-b1b1-8dfc7de8c5f5
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array2D.blit&lt;&#39;T&gt; Function (F#)
Reads a range of elements from the first array and writes them into the second.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array2D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array2D.blit : 'T [,] -> int -> int -> 'T [,] -> int -> int -> int -> int -> unit  
  
// Usage:  
Array2D.blit source sourceIndex1 sourceIndex2 target targetIndex1 targetIndex2 length1 length2  
```  
  
#### Parameters  
 `source`  
 Type: `'T`[&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The source array.  
  
 `sourceIndex1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The first-dimension index to begin copying from in the source array.  
  
 `sourceIndex2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The second-dimension index to begin copying from in the source array.  
  
 `target`  
 Type: `'T`[&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The target array.  
  
 `targetIndex1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The first-dimension index to begin copying into in the target array.  
  
 `targetIndex2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The second-dimension index to begin copying into in the target array.  
  
 `length1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements to copy across the first dimension of the arrays.  
  
 `length2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The number of elements to copy across the second dimension of the arrays.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when any of the indices are negative or if either of the counts are larger than the dimensions of the array allow.|  
  
## Remarks  
 This function is named `CopyTo` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array2D Module (F#)](../vs140/Collections.Array2D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)