---
title: "OperatorIntrinsics.SetArraySlice&lt;&#39;T&gt; Function (F#)"
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
  - OperatorIntrinsics.SetArraySlice<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 05d06b03-85a3-491a-aab5-d15c2c817ec5
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OperatorIntrinsics.SetArraySlice&lt;&#39;T&gt; Function (F#)
Sets a slice of an array.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.OperatorIntrinsics  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
SetArraySlice : 'T [] -> int option -> int option -> 'T [] -> unit  
  
// Usage:  
SetArraySlice target start finish source  
```  
  
#### Parameters  
 `target`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The target array.  
  
 `start`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The start index.  
  
 `finish`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)[option](../vs140/Core.option--T--Type-Abbreviation--F#-.md)  
  
 The end index.  
  
 `source`  
 Type: `'T`[&#91;&#93;](../vs140/Core.--T--Type--F#-2.md)  
  
 The source array.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Operators.OperatorIntrinsics Module (F#)](../vs140/Operators.OperatorIntrinsics-Module--F#-.md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)