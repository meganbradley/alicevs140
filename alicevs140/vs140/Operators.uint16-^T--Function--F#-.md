---
title: "Operators.uint16&lt;^T&gt; Function (F#)"
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
  - Operators.uint16<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5c4e0a16-ac7c-4b69-b599-53b19b0670e3
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.uint16&lt;^T&gt; Function (F#)
Converts the argument to unsigned 16-bit integer. This is a direct conversion for all primitive numeric types. For strings, the input is converted using <xref:System.UInt16.Parse?qualifyHint=False> with <xref:System.Globalization.CultureInfo.InvariantCulture?qualifyHint=False> settings. Otherwise the operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
uint16 : ^T -> uint16 (requires ^T with static member op_Explicit)  
  
// Usage:  
uint16 value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The input value.  
  
## Return Value  
 The converted `uint16` value.  
  
## Remarks  
 This function is named `ToUInt16` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)