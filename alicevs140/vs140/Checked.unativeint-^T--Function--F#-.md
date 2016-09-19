---
title: "Checked.unativeint&lt;^T&gt; Function (F#)"
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
  - Checked.unativeint<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 97cec2c5-0e55-4bbe-826b-219a1c08d3a7
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Checked.unativeint&lt;^T&gt; Function (F#)
Converts the argument to `unativeint`. This is a direct, checked conversion for all primitive numeric types. Otherwise the operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.Checked  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
unativeint : ^T -> unativeint (requires ^T with static member op_Explicit)  
  
// Usage:  
unativeint value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The input value.  
  
## Return Value  
 The converted `unativeint`.  
  
## Remarks  
 This function is named `ToUIntPtr` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Operators.Checked Module (F#)](../Topic/Operators.Checked%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)