---
title: "Operators.float32&lt;^T&gt; Function (F#)"
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
  - Operators.float32<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9603115e-9693-46c1-bf3d-b3d15f2d187a
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.float32&lt;^T&gt; Function (F#)
Converts the argument to 32-bit float. This is a direct conversion for all primitive numeric types. For strings, the input is converted using <xref:System.Single.Parse?qualifyHint=False> with <xref:System.Globalization.CultureInfo.InvariantCulture?qualifyHint=False> settings. Otherwise the operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
float32 : ^T -> float32 (requires ^T with static member op_Explicit)  
  
// Usage:  
float32 value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The input value.  
  
## Return Value  
 The converted `float32` value.  
  
## Remarks  
 This function is named `ToSingle` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)