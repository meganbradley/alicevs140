---
title: "Operators.typeof&lt;&#39;T&gt; Type Function (F#)"
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
  - Operators.typeof<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: ff825d1b-e11d-48d5-9a23-a65e8a170491
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators.typeof&lt;&#39;T&gt; Type Function (F#)
Generate a <xref:System.Type?qualifyHint=False> runtime representation of a static type. The static type is still maintained on the value returned.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.Operators  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
typeof<'T> :  Type  
  
// Usage:  
typeof  
```  
  
## Return Value  
 A <xref:System.Type?qualifyHint=False> object representing the type of the specified expression.  
  
## Remarks  
 This function is named `TypeOf` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.Operators Module (F#)](../Topic/Core.Operators%20Module%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)