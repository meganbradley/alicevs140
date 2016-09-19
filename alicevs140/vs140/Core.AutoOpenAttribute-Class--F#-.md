---
title: "Core.AutoOpenAttribute Class (F#)"
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
  - Core.AutoOpenAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 9e0b39c1-26a2-4bd9-b6a0-9ce7b40dc158
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.AutoOpenAttribute Class (F#)
This attribute is used for two purposes. When applied to an assembly, it must be given a string argument, and this argument must indicate a valid module or namespace in that assembly. Source code files compiled with a reference to this assembly are processed in an environment where the given path is automatically opened.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class ||| AttributeTargets.Assembly, AllowMultiple = true)>]  
[<Sealed>]  
type AutoOpenAttribute =  
 class  
  new AutoOpenAttribute : string -> AutoOpenAttribute  
  new AutoOpenAttribute : unit -> AutoOpenAttribute  
  member this.Path :  string  
 end  
```  
  
## Remarks  
 When applied to a module within an assembly, then the attribute must not be given any arguments. When the enclosing namespace is opened in user source code, the module is also implicitly opened.  
  
 You can also use the short form of the name, `AutoOpen`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.AutoOpenAttribute-Constructor--F#-.md)|Creates an attribute used to mark a namespace or module path to be automatically opened when an assembly is referenced|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Path](../vs140/AutoOpenAttribute.Path-Property--F#-.md)|Indicates the namespace or module to be automatically opened when an assembly is referenced or an enclosing module opened.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)