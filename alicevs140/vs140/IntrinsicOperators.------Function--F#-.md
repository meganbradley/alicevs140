---
title: "IntrinsicOperators.( &amp; ) Function (F#)"
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
ms.assetid: bb78aa6d-71e0-4b22-8a5e-b7d146006ab6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicOperators.( &amp; ) Function (F#)
Computes the Boolean AND operation. When used as a binary operator the right hand value is evaluated only on demand.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( & ) : bool -> bool -> bool  
  
// Usage:  
e1 & e2  
```  
  
#### Parameters  
 `e1`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The first operand.  
  
 `e2`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The second operand.  
  
## Return Value  
 The result of the Boolean AND operation.  
  
## Remarks  
 This function is for use by compiled F# code and should not be used directly.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.IntrinsicOperators Module (F#)](../vs140/LanguagePrimitives.IntrinsicOperators-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)