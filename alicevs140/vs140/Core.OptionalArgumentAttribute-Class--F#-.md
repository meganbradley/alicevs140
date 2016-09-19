---
title: "Core.OptionalArgumentAttribute Class (F#)"
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
  - Core.OptionalArgumentAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1757b4d4-0f46-4c96-94e6-986a744bf7bb
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.OptionalArgumentAttribute Class (F#)
This attribute is added automatically for all optional arguments.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Parameter, AllowMultiple = false)>]  
[<Sealed>]  
type OptionalArgumentAttribute =  
 class  
  new OptionalArgumentAttribute : unit -> OptionalArgumentAttribute  
 end  
```  
  
## Remarks  
 You can apply this attribute to a parameter that is an option type to make it an optional parameter. This is the equivalent of applying a ? to the parameter name in the parameter list. Optional parameters should not be followed by non-optional parameters in the parameter list.  
  
 You can also use the short form of the name, `OptionalArgument`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.OptionalArgumentAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)