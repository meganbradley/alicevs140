---
title: "IntrinsicFunctions.MakeDecimal Function (F#)"
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
ms.assetid: af62eb6c-02c7-487f-bd8d-2ab15c620854
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IntrinsicFunctions.MakeDecimal Function (F#)
This function implements parsing of decimal constants.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.LanguagePrimitives.IntrinsicFunctions  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
MakeDecimal : int -> int -> int -> bool -> byte -> decimal  
  
// Usage:  
MakeDecimal low medium high isNegative scale  
```  
  
#### Parameters  
 `low`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 `medium`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 `high`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 `isNegative`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 `scale`  
 Type: [byte](../Topic/Core.byte%20Type%20Abbreviation%20\(F%23\).md)  
  
## Return Value  
  
## Remarks  
 This function is for use by compiled F# code and should not be used directly.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [LanguagePrimitives.IntrinsicFunctions Module (F#)](../vs140/LanguagePrimitives.IntrinsicFunctions-Module--F#-.md)   
 [Microsoft.FSharp.Core.LanguagePrimitives Namespace (F#)](../Topic/Core.LanguagePrimitives%20Module%20\(F%23\).md)