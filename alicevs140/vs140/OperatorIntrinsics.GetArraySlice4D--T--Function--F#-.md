---
title: "OperatorIntrinsics.GetArraySlice4D&lt;&#39;T&gt; Function (F#)"
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
  - OperatorIntrinsics.GetArraySlice4D<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f12ab1c3-cd76-41bd-888a-736499c3724d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.GetArraySlice4D&lt;&#39;T&gt; Function (F#)
Gets a slice of an array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
GetArraySlice4D : 'T [,,,] -> int option -> int option -> int option -> int option -> int option -> int option -> int option -> int option -> 'T [,,,]  
  
// Usage:  
GetArraySlice4D source start1 finish1 start2 finish2 start3 finish3 start4 finish4  
```  
  
#### Parameters  
 `source`  
 Type: `'T`[&#91;,,,&#93;](../vs140/Core.--T--Type--F#-1.md)  
  
 The source array.  
  
 `start1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the first dimension.  
  
 `finish1`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the first dimension.  
  
 `start2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the second dimension.  
  
 `finish2`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the second dimension.  
  
 `start3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the third dimension.  
  
 `finish3`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the third dimension.  
  
 `start4`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index of the fourth dimension.  
  
 `finish4`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index of the fourth dimension.  
  
## Return Value  
 The four dimensional sub array from the given indices.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Operators.OperatorIntrinsics Module (F#)](../vs140/Operators.OperatorIntrinsics-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)