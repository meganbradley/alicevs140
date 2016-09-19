---
title: "NullableOperators.( ?&gt;=? )&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 3051a50f-d276-4c84-9d73-bf2efeddef94
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NullableOperators.( ?&gt;=? )&lt;&#39;T&gt; Function (F#)
The `>=` operator where a nullable value appears on both left and right sides.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.NullableOperators  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( ?>=? ) : Nullable<'T> -> Nullable<'T> -> bool when 'T : (IComparable) and 'T : (new : unit ->  'T) and 'T : struct and 'T :> ValueType  
  
// Usage:  
nullableValue1 ?>=? nullableValue2  
```  
  
#### Parameters  
 `nullableValue1`  
 Type: <xref:System.Nullable`1?qualifyHint=False><'T>  
  
 The first input value, as a nullable value.  
  
 `nullableValue2`  
 Type: <xref:System.Nullable`1?qualifyHint=False><'T>  
  
 The second input value, as a nullable value.  
  
## Return Value  
 `true` if the first input value is greater than or equal to the second.  
  
## Remarks  
 If either of the input values is null, then the result is `false`.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.NullableOperators Module (F#)](../vs140/Linq.NullableOperators-Module--F#-.md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)