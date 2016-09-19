---
title: "Core.CompiledNameAttribute Class (F#)"
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
  - Core.CompiledNameAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: fb4ca03a-86ae-4334-b6a0-3de01e98904d
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.CompiledNameAttribute Class (F#)
Adding this attribute to a value or function definition in an F# module changes the name used for the value in compiled Common Language Infrastructure (CLI) code.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Method ||| AttributeTargets.Class ||| AttributeTargets.Field ||| AttributeTargets.Interface ||| AttributeTargets.Struct ||| AttributeTargets.Delegate ||| AttributeTargets.Enum ||| AttributeTargets.Property, AllowMultiple = false)>]  
[<Sealed>]  
type CompiledNameAttribute =  
 class  
  new CompiledNameAttribute : string -> CompiledNameAttribute  
  member this.CompiledName :  string  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `CompiledName`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.CompiledNameAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[CompiledName](../vs140/CompiledNameAttribute.CompiledName-Property--F#-.md)|The name of the value as it appears in compiled code.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)