---
title: "Core.RequireQualifiedAccessAttribute Class (F#)"
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
  - Core.RequireQualifiedAccessAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8b9b6ade-0471-4413-ac5d-638cd0de5f15
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.RequireQualifiedAccessAttribute Class (F#)
This attribute is used to indicate that references to the elements of a module, record or union type require explicit qualified access.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type RequireQualifiedAccessAttribute =  
 class  
  new RequireQualifiedAccessAttribute : unit -> RequireQualifiedAccessAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `RequireQualifiedAccess` attribute.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.RequireQualifiedAccessAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)