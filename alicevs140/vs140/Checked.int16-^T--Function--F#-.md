---
title: "Checked.int16&lt;^T&gt; Function (F#)"
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
  - Checked.int16<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 789392fc-85a7-482e-8abb-f0ae68a7042b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Checked.int16&lt;^T&gt; Function (F#)
Converts the argument to `int16`. This is a direct, checked conversion for all primitive numeric types. For strings, the input is converted using <xref:System.Int16.Parse?qualifyHint=False> with <xref:System.Globalization.CultureInfo.InvariantCulture?qualifyHint=False> settings. Otherwise the operation requires an appropriate static conversion method on the input type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.Checked  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
int16 : ^T -> int16 (requires ^T with static member op_Explicit)  
  
// Usage:  
int16 value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The input value.  
  
## Return Value  
 The converted `int16`.  
  
## Remarks  
 This function is named `ToInt16` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Operators.Checked Module (F#)](../Topic/Operators.Checked%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)