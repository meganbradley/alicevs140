---
title: "OperatorIntrinsics.RangeSByte Function (F#)"
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
ms.assetid: a9c350c7-9aa3-4f1a-bd99-3bc76ff67e67
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeSByte Function (F#)
Generates a range of `sbyte` values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeSByte : sbyte -> sbyte -> sbyte -> seq<sbyte>  
  
// Usage:  
RangeSByte start step stop  
```  
  
#### Parameters  
 `start`  
 Type: [sbyte](../Topic/Core.sbyte%20Type%20Abbreviation%20\(F%23\).md)  
  
 The first value of the sequence.  
  
 `step`  
 Type: [sbyte](../Topic/Core.sbyte%20Type%20Abbreviation%20\(F%23\).md)  
  
 The increment between values.  
  
 `stop`  
 Type: [sbyte](../Topic/Core.sbyte%20Type%20Abbreviation%20\(F%23\).md)  
  
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