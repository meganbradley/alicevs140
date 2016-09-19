---
title: "Core.CompilationSourceNameAttribute Class (F#)"
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
  - Core.CompilationSourceNameAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: a191c0ef-160a-4c15-aea6-425198276efd
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.CompilationSourceNameAttribute Class (F#)
This attribute is inserted automatically by the F# compiler to tag methods which are given the [CompiledName](../vs140/Core.CompiledNameAttribute-Class--F#-.md) attribute. It is not intended for use from user code.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.All, AllowMultiple = false)>]  
[<Sealed>]  
type CompilationSourceNameAttribute =  
 class  
  new CompilationSourceNameAttribute : string -> CompilationSourceNameAttribute  
  member this.SourceName :  string  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `CompilationSourceName`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.CompilationSourceNameAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[SourceName](../vs140/CompilationSourceNameAttribute.SourceName-Property--F#-.md)|Indicates the name of the entity in F# source code.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)