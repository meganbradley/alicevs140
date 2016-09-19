---
title: "OperatorIntrinsics.SetArraySlice2DFixed1 Function (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: cf3ce860-1004-4d55-81af-173252c3c398
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.SetArraySlice2DFixed1 Function (F#)
Sets a vector slice of a 2D array. The index of the first dimension is fixed.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
SetArraySlice2DFixed1 : 'T [,] -> int -> int option -> int option -> 'T [] -> unit  
  
// Usage:  
SetArraySlice2DFixed1 target index1 start2 finish2 source  
```  
  
#### Parameters  
 `target`  
 Type: `'T`[&#91;,&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The target array.  
  
 `index1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The start index of the first dimension.  
  
 `start2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the second dimension.  
  
 `finish2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the second dimension.  
  
 `source`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-4.md)  
  
 The source array.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Arrays (F#)](../Topic/Arrays%20\(F%23\).md)   
 [Operators.OperatorIntrinsics Module (F#)](../vs140/Operators.OperatorIntrinsics-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)