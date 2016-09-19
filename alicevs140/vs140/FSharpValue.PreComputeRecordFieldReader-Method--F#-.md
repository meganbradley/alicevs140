---
title: "FSharpValue.PreComputeRecordFieldReader Method (F#)"
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
  - FSharpValue.PreComputeRecordFieldReader
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: bddde908-a749-493c-859c-b41f8fc04646
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpValue.PreComputeRecordFieldReader Method (F#)
Generates a function for reading a particular field from a record.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member PreComputeRecordFieldReader : PropertyInfo -> obj -> obj  
  
// Usage:  
FSharpValue.PreComputeRecordFieldReader (info)  
```  
  
#### Parameters  
 `info`  
 Type: <xref:System.Reflection.PropertyInfo?qualifyHint=False>  
  
 Describes the field to read.  
  
## Exceptions  
  
|Exception|Condition|  
|---------------|---------------|  
|<xref:System.ArgumentException?qualifyHint=False>|Thrown when the input type is not a record type.|  
  
## Return Value  
 A function to read the specified field from the record.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpValue Class (F#)](../Topic/Reflection.FSharpValue%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)