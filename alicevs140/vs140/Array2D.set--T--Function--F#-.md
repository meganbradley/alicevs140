---
title: "Array2D.set&lt;&#39;T&gt; Function (F#)"
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
  - Array2D.set<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c1378409-b257-4833-9a1b-322b618912f1
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array2D.set&lt;&#39;T&gt; Function (F#)
Sets the value of an element in an array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Collections.Array2D  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
Array2D.set : 'T [,] -> int -> int -> 'T -> unit  
  
// Usage:  
Array2D.set array index1 index2 value  
```  
  
#### Parameters  
 `array`  
 Type: `'T`[&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The input array.  
  
 `index1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the first dimension.  
  
 `index2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index along the second dimension.  
  
 `value`  
 Type: `'T`  
  
 The value to set in the array.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the indices are negative or exceed the bounds of the array.|  
  
## Remarks  
 You can also use the syntax `array.[index1,index2] <- value`.  
  
 This function is named `Set` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Collections.Array2D Module (F#)](../vs140/Collections.Array2D-Module--F#-.md)   
 [Microsoft.FSharp.Collections Namespace (F#)](../Topic/Microsoft.FSharp.Collections%20Namespace%20\(F%23\).md)