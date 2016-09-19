---
title: "OperatorIntrinsics.RangeGeneric&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 51f3890d-ddab-4281-adb3-ffecec4e8196
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.RangeGeneric&lt;&#39;T&gt; Function (F#)
Generates a range of values using the given zero, add, start, step and stop values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
RangeGeneric : 'T -> ('T -> 'T -> 'T) -> 'T -> 'T -> seq<'T>  
  
// Usage:  
RangeGeneric one add start stop  
```  
  
#### Parameters  
 `one`  
 Type: `'T`  
  
 The value representing 1 for the type parameter.  
  
 `add`  
 Type: `'T -> 'T -> 'T`  
  
 A function that performs addition to the type parameter.  
  
 `start`  
 Type: `'T`  
  
 The start of the range.  
  
 `stop`  
 Type: `'T`  
  
 The end of the range.  
  
## Return Value  
 An enumerable sequence representing a range of values.  
  
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