---
title: "FSharpValue.GetTupleField Method (F#)"
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
  - FSharpValue.GetTupleField
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: db833e2d-be73-40b8-af89-bc273e40fa06
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpValue.GetTupleField Method (F#)
Reads a field from a tuple value.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member GetTupleField : obj * int -> obj  
  
// Usage:  
FSharpValue.GetTupleField (tuple, index)  
```  
  
#### Parameters  
 `tuple`  
 Type: [obj](../Topic/Core.obj%20Type%20Abbreviation%20\(F%23\).md)  
  
 The input tuple.  
  
 `index`  
 Type: [int](../vs140/Core.int-Type-Abbreviation--F#-.md)  
  
 The index of the field to read.  
  
## Return Value  
 The value of the field.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpValue Class (F#)](../Topic/Reflection.FSharpValue%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)