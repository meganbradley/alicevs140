---
title: "Operators.not Function (F#)"
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
  - Operators.not
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d6962f70-3a4a-4dba-8d54-bb0b95fe1348
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.not Function (F#)
Negate a logical value. `not``true` equals `false` and `not``false` equals `true`.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
not : bool -> bool  
  
// Usage:  
not value  
```  
  
#### Parameters  
 `value`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 The value to negate.  
  
## Return Value  
 The result of the negation.  
  
## Remarks  
 This function is named `Not` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)