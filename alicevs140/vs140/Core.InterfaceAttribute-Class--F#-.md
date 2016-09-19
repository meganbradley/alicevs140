---
title: "Core.InterfaceAttribute Class (F#)"
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
  - Core.InterfaceAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 19860f07-4922-4fd0-9d84-2c1b35a6ee62
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.InterfaceAttribute Class (F#)
Adding this attribute to a type causes it to be represented using a .NET Framework interface.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Interface, AllowMultiple = false)>]  
[<Sealed>]  
type InterfaceAttribute =  
 class  
  new InterfaceAttribute : unit -> InterfaceAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `Interface`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.InterfaceAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)