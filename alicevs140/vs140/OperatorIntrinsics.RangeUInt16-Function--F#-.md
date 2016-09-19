---
title: "OperatorIntrinsics.RangeUInt16 Function (F#)"
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
ms.assetid: 832552ea-57db-4f0a-a43c-d7c244ffaf09
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeUInt16 Function (F#)
Generates a range of `uint16` values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeUInt16 : uint16 -> uint16 -> uint16 -> seq<uint16>  
  
// Usage:  
RangeUInt16 start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [uint16](../vs140/Core.uint16-Type-Abbreviation--F#-.md)  
  
 The starting value of the sequence.  
  
 `step`  
 Type: [uint16](../vs140/Core.uint16-Type-Abbreviation--F#-.md)  
  
 The increment between values.  
  
 `stop`  
 Type: [uint16](../vs140/Core.uint16-Type-Abbreviation--F#-.md)  
  
 The maximum value of the sequence.  
  
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