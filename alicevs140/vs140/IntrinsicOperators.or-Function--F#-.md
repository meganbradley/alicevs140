---
title: "IntrinsicOperators.or Function (F#)"
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
ms.assetid: 17443474-fee0-4292-8df4-970e14cfcf28
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicOperators.or Function (F#)
Binary `or`. When used as a binary operator the right hand value is evaluated only on demand.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicOperators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
or : bool -> bool -> bool  
  
// Usage:  
or e1 e2  
```  
  
#### Parameters  
 `e1`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The first operand.  
  
 `e2`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The second operand.  
  
## Return Value  
 The result of the Boolean OR operation.  
  
## Remarks  
 This function is for use by compiled F# code and should not be used directly.  
  
 This function is named `Or` in compiled assemblies. If you are accessing the member from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.IntrinsicOperators Module (F#)](../vs140/LanguagePrimitives.IntrinsicOperators-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)