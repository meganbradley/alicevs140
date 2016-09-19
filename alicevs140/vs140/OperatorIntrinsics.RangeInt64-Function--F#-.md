---
title: "OperatorIntrinsics.RangeInt64 Function (F#)"
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
ms.assetid: e1051964-6ee5-44c9-aa12-39c28244ae73
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeInt64 Function (F#)
Generate a range of `int64` values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeInt64 : int64 -> int64 -> int64 -> seq<int64>  
  
// Usage:  
RangeInt64 start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [int64](../vs140/Core.int64-Type-Abbreviation--F#-.md)  
  
 The first value in the sequence.  
  
 `step`  
 Type: [int64](../vs140/Core.int64-Type-Abbreviation--F#-.md)  
  
 The increment between each value.  
  
 `stop`  
 Type: [int64](../vs140/Core.int64-Type-Abbreviation--F#-.md)  
  
 The maximum value in the sequence.  
  
## Return Value  
 An enumerable collection of values.  
  
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