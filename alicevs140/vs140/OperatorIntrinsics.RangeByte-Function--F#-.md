---
title: "OperatorIntrinsics.RangeByte Function (F#)"
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
ms.assetid: 6a7e4d3e-93f4-408b-b365-bee6710e9d7e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeByte Function (F#)
Generates a range of `byte` values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeByte : byte -> byte -> byte -> seq<byte>  
  
// Usage:  
RangeByte start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [byte](../Topic/Core.byte%20Type%20Abbreviation%20\(F%23\).md)  
  
 The first value in the sequence.  
  
 `step`  
 Type: [byte](../Topic/Core.byte%20Type%20Abbreviation%20\(F%23\).md)  
  
 An increment between each value.  
  
 `stop`  
 Type: [byte](../Topic/Core.byte%20Type%20Abbreviation%20\(F%23\).md)  
  
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