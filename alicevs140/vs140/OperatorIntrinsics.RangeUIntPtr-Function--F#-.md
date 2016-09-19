---
title: "OperatorIntrinsics.RangeUIntPtr Function (F#)"
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
ms.assetid: 25cb7163-9d14-495c-b5d0-acbddb578180
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeUIntPtr Function (F#)
Generates a range of `unativeint` values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeUIntPtr : unativeint -> unativeint -> unativeint -> seq<unativeint>  
  
// Usage:  
RangeUIntPtr start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [unativeint](../vs140/Core.unativeint-Type-Abbreviation--F#-.md)  
  
 The first value in the sequence.  
  
 `step`  
 Type: [unativeint](../vs140/Core.unativeint-Type-Abbreviation--F#-.md)  
  
 The increment between values.  
  
 `stop`  
 Type: [unativeint](../vs140/Core.unativeint-Type-Abbreviation--F#-.md)  
  
 The maximum value in the sequence.  
  
## Return Value  
 A sequence of enumerable values.  
  
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