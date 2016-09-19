---
title: "Operators.sign&lt;^T&gt; Function (F#)"
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
  - Operators.sign<^T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f45dd870-f208-4b7c-b9d3-7bfbf783124e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.sign&lt;^T&gt; Function (F#)
Sign of the given number.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
sign : ^T -> int (requires ^T with member Sign)  
  
// Usage:  
sign value  
```  
  
#### Parameters  
 `value`  
 Type: `^T`  
  
 The input value.  
  
## Return Value  
 -1, 0, or 1 depending on the sign of the input.  
  
## Remarks  
 This function is named `Sign` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)