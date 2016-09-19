---
title: "LanguagePrimitives.DivideByIntDynamic&lt;&#39;T&gt; Function (F#)"
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
ms.assetid: 32d5d11f-0742-4a96-a76a-6a373e8ab92c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LanguagePrimitives.DivideByIntDynamic&lt;&#39;T&gt; Function (F#)
A compiler intrinsic that implements dynamic invocations for the [DivideByInt](../vs140/LanguagePrimitives.DivideByInt-^T--Function--F#-.md) primitive.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
DivideByIntDynamic : 'T -> int -> 'T  
  
// Usage:  
DivideByIntDynamic x y  
```  
  
#### Parameters  
 `x`  
 Type: `'T`  
  
 The dividend, or numerator.  
  
 `y`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The divisor, or denominator.  
  
## Return Value  
 The quotient.  
  
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