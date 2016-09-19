---
title: "LanguagePrimitives.CheckedMultiplyDynamic&lt;&#39;T1,&#39;T2,&#39;U&gt; Function (F#)"
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
ms.assetid: 1d4117f7-8bec-4a38-905b-6da4855d4322
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.CheckedMultiplyDynamic&lt;&#39;T1,&#39;T2,&#39;U&gt; Function (F#)
A compiler intrinsic that implements dynamic invocations to the checked `*` operator.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
CheckedMultiplyDynamic : 'T1 -> 'T2 -> 'U  
  
// Usage:  
CheckedMultiplyDynamic x y  
```  
  
#### Parameters  
 `x`  
 Type: `'T1`  
  
 The first operand.  
  
 `y`  
 Type: `'T2`  
  
 The second operand.  
  
## Return Value  
 The product of the operands.  
  
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