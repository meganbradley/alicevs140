---
title: "Operators.defaultArg&lt;&#39;T&gt; Function (F#)"
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
  - Operators.defaultArg<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 926539d7-bee7-444c-96db-9ef382b0b535
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.defaultArg&lt;&#39;T&gt; Function (F#)
Used to specify a default value for an optional argument in the implementation of a function.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
defaultArg : 'T option -> 'T -> 'T  
  
// Usage:  
defaultArg arg defaultValue  
```  
  
#### Parameters  
 `arg`  
 Type: `'T option`  
  
 An option representing the argument.  
  
 `defaultValue`  
 Type: `'T`  
  
 The default value of the argument.  
  
## Return Value  
 The argument value. If it is `None`, the `defaultValue` is returned.  
  
## Remarks  
 This function is named `DefaultArg` in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)