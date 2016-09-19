---
title: "LanguagePrimitives.AdditionDynamic&lt;&#39;T1,&#39;T2,&#39;U&gt; Function (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 194d2028-9542-4331-9d64-f2a18c08fa9a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.AdditionDynamic&lt;&#39;T1,&#39;T2,&#39;U&gt; Function (F#)
A compiler intrinsic that implements dynamic invocations of the `+` operator.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
AdditionDynamic : 'T1 -> 'T2 -> 'U  
  
// Usage:  
AdditionDynamic x y  
```  
  
#### Parameters  
 `x`  
 Type: `'T1`  
  
 The first operand.  
  
 `y`  
 Type: `'T2`  
  
 The second operand.  
  
## Return Value  
 The sum of the operands.  
  
## Remarks  
 This function is for use by compiled F# code and should not be used directly.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.LanguagePrimitives Module (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)