---
title: "Checked.( - )&lt;^T1,^T2,^T3&gt; Function (F#)"
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
  - Checked.( - )<^T1,^T2,^T3>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7c16d973-2ab5-4689-8f01-2fd3a79fe536
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Checked.( - )&lt;^T1,^T2,^T3&gt; Function (F#)
Overloaded subtraction operator (checks for overflow).  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators.Checked  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( - ) : ^T1 -> ^T2 -> ^T3 (requires ^T1 with static member (-) and ^T2 with static member (-))  
  
// Usage:  
x - y  
```  
  
#### Parameters  
 `x`  
 Type: `^T1`  
  
 The first value.  
  
 `y`  
 Type: `^T2`  
  
 The second value.  
  
## Return Value  
 The first value minus the second value.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Operators.Checked Module (F#)](../Topic/Operators.Checked%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core.Operators Namespace (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)