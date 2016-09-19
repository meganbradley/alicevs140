---
title: "FSharpType.IsFunction Method (F#)"
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
  - FSharpType.IsFunction
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 98a858ba-7be9-4e2f-924e-5c876272a6a7
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpType.IsFunction Method (F#)
Returns `true` if the specified type is a representation of an F# function type or the runtime type of a closure implementing an F# function type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Reflection  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member IsFunction : Type -> bool  
  
// Usage:  
FSharpType.IsFunction (typ)  
```  
  
#### Parameters  
 `typ`  
 Type: <xref:System.Type?qualifyHint=False>  
  
 The type to check.  
  
## Return Value  
 Returns `true` if the type check succeeds.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Reflection.FSharpType Class (F#)](../Topic/Reflection.FSharpType%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Reflection Namespace (F#)](../vs140/Microsoft.FSharp.Reflection-Namespace--F#-.md)