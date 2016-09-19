---
title: "Operators.enum&lt;^U&gt; Function (F#)"
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
  - Operators.enum<^U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ece84451-8d9b-4030-b7f4-1265e0940bd3
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.enum&lt;^U&gt; Function (F#)
Converts the argument to a particular `enum` type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
enum : int32 -> ^U (requires enum)  
  
// Usage:  
enum value  
```  
  
#### Parameters  
 `value`  
 Type: [int32](../Topic/Core.int32%20Type%20Abbreviation%20\(F%23\).md)  
  
 The input value.  
  
## Return Value  
 The converted `enum` type.  
  
## Remarks  
 This function is named `ToEnum` in the compiled assembly. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)