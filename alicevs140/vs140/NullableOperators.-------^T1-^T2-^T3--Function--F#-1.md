---
title: "NullableOperators.( ?- )&lt;^T1,^T2,^T3&gt; Function (F#)1"
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
H1: NullableOperators.( ?- )&lt;^T1,^T2,^T3&gt; Function (F#)
ms.assetid: f237a7a6-89f2-48b2-a2fe-f0b98a2bedc2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NullableOperators.( ?- )&lt;^T1,^T2,^T3&gt; Function (F#)1
The subtraction operator where a nullable value appears on the left.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.NullableOperators  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( ?- ) : Nullable<^T1> -> ^T2 -> Nullable<^T3> when ^T1 with static member (-) and ^T1 : (new : unit ->  ^T1) and ^T1 : struct and ^T1 :> ValueType and ^T2 with static member (-) and ^T3 : (new : unit ->  ^T3) and ^T3 : struct and ^T3 :> ValueType  
  
// Usage:  
nullableValue ?- value  
```  
  
#### Parameters  
 `nullableValue`  
 Type: <xref:System.Nullable`1?qualifyHint=False><^T1>  
  
 The first input value, as a nullable value.  
  
 `value`  
 Type: ^T2  
  
 The second input value.  
  
## Return Value  
 The result of the subtraction, as a nullable value.  
  
## Remarks  
 If the first value is null, then the result is null, as a nullable value.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.02.0, 4.0, Portable  
  
## See Also  
 [Linq.NullableOperators Module (F#)](../vs140/Linq.NullableOperators-Module--F#-.md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)