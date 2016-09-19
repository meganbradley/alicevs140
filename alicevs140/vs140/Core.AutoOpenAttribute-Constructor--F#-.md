---
title: "Core.AutoOpenAttribute Constructor (F#)"
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
  - AutoOpenAttribute.AutoOpenAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d9c945f1-074f-401d-a9c1-1949e3f8170f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.AutoOpenAttribute Constructor (F#)
Creates an attribute used to mark a namespace or module path to be automatically opened when an assembly is referenced.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:  
new AutoOpenAttribute : string -> AutoOpenAttribute  
new AutoOpenAttribute : unit -> AutoOpenAttribute  
  
// Usage:  
new AutoOpenAttribute (path)  
new AutoOpenAttribute ()  
```  
  
#### Parameters  
 `path`  
 Type: [string](../vs140/Core.string-Type-Abbreviation--F#-.md)  
  
 The namespace or module to be automatically opened when an assembly is referenced or an enclosing module opened.  
  
## Return Value  
 A new `AutoOpenAttribute` instance.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.AutoOpenAttribute Class (F#)](../vs140/Core.AutoOpenAttribute-Class--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)