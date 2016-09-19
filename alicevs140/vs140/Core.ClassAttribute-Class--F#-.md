---
title: "Core.ClassAttribute Class (F#)"
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
  - Core.ClassAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 956bd710-c547-4fb8-a0db-6b82753739bc
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.ClassAttribute Class (F#)
Adding this attribute to a type causes it to be represented using a Common Language Infrastructure (CLI) class.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type ClassAttribute =  
 class  
  new ClassAttribute : unit -> ClassAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `Class`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.ClassAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)