---
title: "OperatorIntrinsics.GetStringSlice Function (F#)"
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
  - OperatorIntrinsics.GetStringSlice
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d119e7b4-a35f-4597-ada7-013294f2511b
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.GetStringSlice Function (F#)
Gets a slice from a string.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GetStringSlice : string -> int option -> int option -> string  
  
// Usage:  
GetStringSlice source start finish  
```  
  
#### Parameters  
 `source`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The source string.  
  
 `start`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The index of the first character of the slice.  
  
 `finish`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The index of the last character of the slice.  
  
## Return Value  
 The substring from the given indices.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Operators.OperatorIntrinsics Module (F#)](../vs140/Operators.OperatorIntrinsics-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)