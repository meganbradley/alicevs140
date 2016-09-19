---
title: "NullableOperators.( ?=? )&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 5f793f29-1084-4570-b1c1-17c1b7ef764b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NullableOperators.( ?=? )&lt;&#39;T&gt; Function (F#)
The `=` operator where a nullable value appears on both left and right sides.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.NullableOperators  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( ?=? ) : Nullable<'T> -> Nullable<'T> -> bool when 'T : equality and 'T : (new : unit ->  'T) and 'T : struct and 'T :> ValueType  
  
// Usage:  
 nullableValue1 ?=? nullableValue2  
```  
  
#### Parameters  
 `nullableValue1`  
 Type: <xref:System.Nullable`1?qualifyHint=False><'T>  
  
 The first input value, as a nullable value.  
  
 `nullableValue2`  
 Type: <xref:System.Nullable`1?qualifyHint=False><'T>  
  
 The second input value, as a nullable value.  
  
## Return Value  
 True if the input values are numerically equal.  
  
## Remarks  
 If either of the values is null, the result is `false`. Even if both sides are null, the result is `false`.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.NullableOperators Module (F#)](../vs140/Linq.NullableOperators-Module--F#-.md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)