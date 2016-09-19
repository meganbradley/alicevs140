---
title: "Operators.using&lt;&#39;T,&#39;U&gt; Function (F#)"
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
  - Operators.using<'T,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: de177834-c364-4a08-967b-8bd9dea1979d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.using&lt;&#39;T,&#39;U&gt; Function (F#)
Clean up resources associated with the input object after the completion of the given function. Cleanup occurs even when an exception is raised by the protected code.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
using : 'T -> ('T -> 'U) -> 'U (requires 'T :> IDisposable)  
  
// Usage:  
using resource action  
```  
  
#### Parameters  
 `resource`  
 Type: `'T`  
  
 The resource to be disposed after action is called.  
  
 `action`  
 Type: `'T -> 'U`  
  
 The action that accepts the resource.  
  
## Return Value  
 The resulting value.  
  
## Remarks  
 This function is named `Using` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)