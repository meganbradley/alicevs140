---
title: "Operators.failwith&lt;&#39;T&gt; Function (F#)"
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
  - Operators.failwith<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b168262a-4e63-4c9e-82c7-b952276a36be
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.failwith&lt;&#39;T&gt; Function (F#)
Throw a `T:System.Exception` exception.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
failwith : string -> 'T  
  
// Usage:  
failwith message  
```  
  
#### Parameters  
 `message`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The exception message.  
  
## Return Value  
 The result value.  
  
## Remarks  
 This function is named `FailWith` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)