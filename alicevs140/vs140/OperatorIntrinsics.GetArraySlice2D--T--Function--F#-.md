---
title: "OperatorIntrinsics.GetArraySlice2D&lt;&#39;T&gt; Function (F#)"
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
  - OperatorIntrinsics.GetArraySlice2D<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 4b231cd3-cbd1-4eca-a3cb-4b21f9feda7e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.GetArraySlice2D&lt;&#39;T&gt; Function (F#)
Gets a slice of an array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GetArraySlice2D : 'T [,] -> int option -> int option -> int option -> int option -> 'T [,]  
  
// Usage:  
GetArraySlice2D source start1 finish1 start2 finish2  
```  
  
#### Parameters  
 `source`  
 Type: `'T`[&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The source array.  
  
 `start1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the first dimension.  
  
 `finish1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the first dimension.  
  
 `start2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the second dimension.  
  
 `finish2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the second dimension.  
  
## Return Value  
 The two dimensional sub array from the input indices.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Operators.OperatorIntrinsics Module (F#)](../vs140/Operators.OperatorIntrinsics-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)