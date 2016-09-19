---
title: "Operators.( .. )&lt;^T&gt; Function (F#)"
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
  - Operators.( .. )<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ebe9fda6-3706-4eb7-96c9-2b1389f6c138
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.( .. )&lt;^T&gt; Function (F#)
The standard overloaded range operator, for example, `[n..m]` for lists, `seq {n..m}` for sequences.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( .. ) : ^T -> ^T -> seq<^T> (requires ^T with static member (+) and ^T with static member One)  
  
// Usage:  
start .. finish  
```  
  
#### Parameters  
 `start`  
 Type: `^T`  
  
 The start value of the range.  
  
 `finish`  
 Type: `^T`  
  
 The end value of the range.  
  
## Return Value  
 The sequence spanning the range.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)