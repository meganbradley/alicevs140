---
title: "Operators.( ^ ) Function (F#)"
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
  - Operators.( ^ )
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: f7078883-8fca-4cc8-a2ab-54127fba6f96
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.( ^ ) Function (F#)
Concatenate two strings. The operator [+](../vs140/Operators.------^T1-^T2-^T3--Function--F#-.md) should be used instead.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
( ^ ) : string -> string -> string  
  
// Usage:  
s1 ^ s2  
```  
  
#### Parameters  
 `s1`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 `s2`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
## Return Value  
  
## Remarks  
 This operator is provided for compatibility with other versions of ML, and generates a warning when used unless you use the `--mlcompatibility` compiler option. For more information, see [Compiler Options (F#)](../vs140/Compiler-Options--F#-.md).  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)