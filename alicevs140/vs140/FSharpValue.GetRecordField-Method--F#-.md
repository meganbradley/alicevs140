---
title: "FSharpValue.GetRecordField Method (F#)"
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
  - FSharpValue.GetRecordField
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 6dacc2db-7425-45c0-bb04-77b84dd0452a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpValue.GetRecordField Method (F#)
Reads a field from a record value.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member GetRecordField : obj * PropertyInfo -> obj  
  
// Usage:  
FSharpValue.GetRecordField (record, info)  
```  
  
#### Parameters  
 `record`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The record object.  
  
 `info`  
 Type: <xref:System.Reflection.PropertyInfo?qualifyHint=False>  
  
 The <xref:System.Reflection.PropertyInfo?qualifyHint=False> object describing the field to read.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input type is not a record type.|  
  
## Return Value  
 The field from the record.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpValue Class (F#)](../Topic/Reflection.FSharpValue%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)