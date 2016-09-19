---
title: "Checked.uint64&lt;^T&gt; Function (F#)"
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
  - Checked.uint64<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 70fa85e1-3322-4514-a145-fbad90ae9667
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Checked.uint64&lt;^T&gt; Function (F#)
Converts the argument to `uint64`. This is a direct, checked conversion for all primitive numeric types. For strings, the input is converted using <xref:System.UInt64.Parse?qualifyHint=False> with InvariantCulture settings. Otherwise the operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.Checked  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
uint64 : ^T -> uint64 (requires ^T with static member op_Explicit)  
  
// Usage:  
uint64 value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The input value.  
  
## Return Value  
 The converted `uint64`.  
  
## Remarks  
 This function is named `ToUInt64` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Operators.Checked Module (F#)](../Topic/Operators.Checked%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)