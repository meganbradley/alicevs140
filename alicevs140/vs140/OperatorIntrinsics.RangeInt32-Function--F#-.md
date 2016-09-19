---
title: "OperatorIntrinsics.RangeInt32 Function (F#)"
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
ms.assetid: cd6909aa-e3c5-4d25-8092-c972c423ee10
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeInt32 Function (F#)
Generate a range of integers.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeInt32 : int -> int -> int -> seq<int>  
  
// Usage:  
RangeInt32 start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The starting integer.  
  
 `step`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The increment between each integer.  
  
 `stop`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The ending integer, which is included in the range.  
  
## Return Value  
  
## Remarks  
 This function is for use by compiled F# code and should not be used directly.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Operators.OperatorIntrinsics Module (F#)](../vs140/Operators.OperatorIntrinsics-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)