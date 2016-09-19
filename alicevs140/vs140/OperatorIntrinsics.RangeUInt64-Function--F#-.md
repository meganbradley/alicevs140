---
title: "OperatorIntrinsics.RangeUInt64 Function (F#)"
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
ms.assetid: e4dd4711-e51b-475b-89c7-f531e14bfe6c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeUInt64 Function (F#)
Generates a range of uint64 values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeUInt64 : uint64 -> uint64 -> uint64 -> seq<uint64>  
  
// Usage:  
RangeUInt64 start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [uint64](../vs140/Core.uint64-Type-Abbreviation--F#-.md)  
  
 The initial value in the sequence.  
  
 `step`  
 Type: [uint64](../vs140/Core.uint64-Type-Abbreviation--F#-.md)  
  
 The increment between each value.  
  
 `stop`  
 Type: [uint64](../vs140/Core.uint64-Type-Abbreviation--F#-.md)  
  
 The maximum value in the sequence.  
  
## Return Value  
 An enumerable sequence of values.  
  
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