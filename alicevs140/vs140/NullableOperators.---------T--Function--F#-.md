---
title: "NullableOperators.( &lt;&gt;? )&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 3179aace-70c4-4911-9258-619592214976
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NullableOperators.( &lt;&gt;? )&lt;&#39;T&gt; Function (F#)
The `<>` operator where a nullable value appears on the right.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq.NullableOperators  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( <>? ) : 'T -> Nullable<'T> -> bool when 'T : (IComparable) and 'T : (new : unit ->  'T) and 'T : struct and 'T :> ValueType  
  
// Usage:  
value <>? nullableValue  
```  
  
#### Parameters  
 `value`  
 Type: <xref:System.Nullable`1?qualifyHint=False><'T>  
  
 The first input value.  
  
 `nullableValue`  
 Type: 'T  
  
 The second input value, as a nullable value.  
  
## Return Value  
 `true` if the two input values are not numerically equal; otherwise, `false`.  
  
## Remarks  
 If the second value is null, the result is `false`.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.NullableOperators Module (F#)](../vs140/Linq.NullableOperators-Module--F#-.md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)