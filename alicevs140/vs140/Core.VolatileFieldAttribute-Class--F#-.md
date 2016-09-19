---
title: "Core.VolatileFieldAttribute Class (F#)"
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
  - Core.VolatileFieldAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1e7ea0f8-4c85-402e-b529-55079bc79d7e
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.VolatileFieldAttribute Class (F#)
Adding this attribute to an F# mutable binding causes the `volatile` prefix to be used for all accesses to the field.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Field, AllowMultiple = false)>]  
[<Sealed>]  
type VolatileFieldAttribute =  
 class  
  new VolatileFieldAttribute : unit -> VolatileFieldAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `VolatileField`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.VolatileFieldAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)