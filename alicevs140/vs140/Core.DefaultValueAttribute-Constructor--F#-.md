---
title: "Core.DefaultValueAttribute Constructor (F#)"
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
  - DefaultValueAttribute.DefaultValueAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 14c22e07-b5a8-40fe-9363-30d397b09c44
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.DefaultValueAttribute Constructor (F#)
Creates an instance of the attribute.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:  
new DefaultValueAttribute : bool -> DefaultValueAttribute  
new DefaultValueAttribute : unit -> DefaultValueAttribute  
  
// Usage:  
new DefaultValueAttribute (check)  
new DefaultValueAttribute ()  
```  
  
#### Parameters  
 `check`  
 Type: [bool](../Topic/Core.bool%20Type%20Abbreviation%20\(F%23\).md)  
  
 Indicates whether to assert that the field type supports `null`.  
  
## Return Value  
 A new `DefaultValueAttribute` instance.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.DefaultValueAttribute Class (F#)](../Topic/Core.DefaultValueAttribute%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)