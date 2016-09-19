---
title: "CancellationTokenRegistration.( = ) Method (F#)"
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
  - CancellationTokenRegistration.( == )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b5a5bdc1-3015-4155-90d5-619dab2e1d85
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CancellationTokenRegistration.( = ) Method (F#)
Equality operator for registrations.  
  
 **Namespace/Module Path**: System.Threading  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member ( = ) : CancellationTokenRegistration * CancellationTokenRegistration -> bool  
  
// Usage:  
registration1 = registration2  
```  
  
#### Parameters  
 `registration1`  
 Type: [CancellationTokenRegistration](../Topic/Threading.CancellationTokenRegistration%20Structure%20\(F%23\).md)  
  
 The first input registration.  
  
 `registration2`  
 Type: [CancellationTokenRegistration](../Topic/Threading.CancellationTokenRegistration%20Structure%20\(F%23\).md)  
  
 The second input registration.  
  
## Return Value  
 True if the two registrations are equal.  
  
## Remarks  
 This API is provided for use only with the F# Core Library Versions that targets .NET Framework 2.0. If you are using .NET Framework 4, use the .NET Framework 4 API with the same name, <xref:System.Threading.CancellationTokenRegistration.op_Equality?qualifyHint=False>.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0  
  
## See Also  
 [Threading.CancellationTokenRegistration Structure (F#)](../Topic/Threading.CancellationTokenRegistration%20Structure%20\(F%23\).md)   
 [System.Threading Namespace (F#)](../Topic/System.Threading%20Namespace%20\(F%23\).md)