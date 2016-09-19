---
title: "Core.CLIMutableAttribute Class (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 571d62f3-5fb5-4088-a9d8-9d2fa61efdb7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.CLIMutableAttribute Class (F#)
Adding this attribute to a record type causes it to be compiled to a Common Language Infrastructure (CLI) representation with a default constructor with property getters and setters.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>][<Sealed>]type CLIMutableAttribute = class  new CLIMutableAttribute : unit -> CLIMutableAttribute end  
```  
  
## Remarks  
 You can also use the short form of the name, CLIMutable.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.CLIMutableAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)