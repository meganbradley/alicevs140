---
title: "FSharpValue.GetUnionFields Method (F#)"
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
  - FSharpValue.GetUnionFields
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ba1e1a92-cfd1-4f70-9316-ffe940e1bca0
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpValue.GetUnionFields Method (F#)
Identify the union case and its fields for an object.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member GetUnionFields : obj * Type * ?BindingFlags -> UnionCaseInfo * obj []  
static member GetUnionFields : obj * Type * ?bool -> UnionCaseInfo * obj []  
  
// Usage:  
FSharpValue.GetUnionFields (value, unionType)  
FSharpValue.GetUnionFields (value, unionType, bindingFlags = bindingFlags)  
  
open FSharpReflectionExtensions  
FSharpValue.GetUnionFields (value, unionType, allowAccessToPrivateRepresentation = false)  
```  
  
#### Parameters  
 `value`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The input union case.  
  
 `unionType`  
 Type: <xref:System.Type?qualifyHint=False>  
  
 The union type containing the value.  
  
 `bindingFlags`  
 Type: <xref:System.Reflection.BindingFlags?qualifyHint=False>  
  
 Optional binding flags.  
  
 `allowAccessToPrivateRepresentation`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 Optional flag that denotes accessibility of the private representation.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input type is not a union case value.|  
  
## Return Value  
 The description of the union case (as a [UnionCaseInfo](../Topic/Reflection.UnionCaseInfo%20Class%20\(F%23\).md)object) and its fields.  
  
## Remarks  
 If the type is not given, then the runtime type of the input object is used to identify the relevant union type. The type should always be given if the input object may be `null`. For example, option values may be represented using the `null`.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpValue Class (F#)](../Topic/Reflection.FSharpValue%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)