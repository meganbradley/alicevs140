---
title: "FSharpValue.PreComputeRecordConstructorInfo Method (F#)"
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
  - FSharpValue.PreComputeRecordConstructorInfo
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 301602a5-664d-4c93-9875-f795c6c0b3e4
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpValue.PreComputeRecordConstructorInfo Method (F#)
Gets a <xref:System.Reflection.ConstructorInfo?qualifyHint=False> object for a record type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member PreComputeRecordConstructorInfo : Type * ?BindingFlags -> ConstructorInfo  
static member PreComputeRecordConstructorInfo : Type * ?bool -> ConstructorInfo  
  
// Usage:  
FSharpValue.PreComputeRecordConstructorInfo (recordType)  
FSharpValue.PreComputeRecordConstructorInfo (recordType, bindingFlags = bindingFlags)  
  
open FSharpReflectionExtensions  
FSharpValue.PreComputeRecordConstructorInfo (recordType, allowAccessToPrivateRepresentation = false)  
```  
  
#### Parameters  
 `recordType`  
 Type: <xref:System.Type?qualifyHint=False>  
  
 The record type.  
  
 `bindingFlags`  
 Type: <xref:System.Reflection.BindingFlags?qualifyHint=False>  
  
 Optional binding flags.  
  
 `allowAccessToPrivateRepresentation`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 Optional flag that denotes accessibility of the private representation.  
  
## Return Value  
 A <xref:System.Reflection.ConstructorInfo?qualifyHint=False> object for the given record type.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpValue Class (F#)](../Topic/Reflection.FSharpValue%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)