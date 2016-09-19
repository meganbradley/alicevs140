---
title: "OperatorIntrinsics.RangeChar Function (F#)"
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
ms.assetid: 720a3896-38c6-464a-bff7-7509095fcf68
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeChar Function (F#)
Generates a range of `char` values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeChar : char -> char -> seq<char>  
  
// Usage:  
RangeChar start stop  
```  
  
#### Parameters  
 `start`  
 Type: [char](../Topic/Core.char%20Type%20Abbreviation%20\(F%23\).md)  
  
 The first value in the sequence.  
  
 `stop`  
 Type: [char](../Topic/Core.char%20Type%20Abbreviation%20\(F%23\).md)  
  
 The last value in the sequence.  
  
## Return Value  
 An enumerable sequence of `char` values.  
  
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