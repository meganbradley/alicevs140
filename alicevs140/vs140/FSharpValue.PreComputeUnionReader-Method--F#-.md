---
title: "FSharpValue.PreComputeUnionReader Method (F#)"
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
  - FSharpValue.PreComputeUnionReader
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 3229aed9-fb5c-4c94-ae83-7a730776ff2e
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpValue.PreComputeUnionReader Method (F#)
Generates a function for reading all the fields for a particular discriminator case of a union type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member PreComputeUnionReader : UnionCaseInfo * ?BindingFlags -> obj -> obj []  
static member PreComputeUnionReader : UnionCaseInfo * ?bool -> obj -> obj []  
  
// Usage:  
FSharpValue.PreComputeUnionReader (unionCase)  
FSharpValue.PreComputeUnionReader (unionCase, bindingFlags = bindingFlags)  
  
open FSharpReflectionExtensions  
FSharpValue.PreComputeUnionReader (unionCase, allowAccessToPrivateRepresentation = false)  
```  
  
#### Parameters  
 `unionCase`  
 Type: [UnionCaseInfo](../Topic/Reflection.UnionCaseInfo%20Class%20\(F%23\).md)  
  
 The description of the union case to read.  
  
 `bindingFlags`  
 Type: <xref:System.Reflection.BindingFlags?qualifyHint=False>  
  
 Optional binding flags.  
  
 `allowAccessToPrivateRepresentation`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 Optional flag that denotes accessibility of the private representation.  
  
## Return Value  
 A function to for reading the fields of the given union case.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpValue Class (F#)](../Topic/Reflection.FSharpValue%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)