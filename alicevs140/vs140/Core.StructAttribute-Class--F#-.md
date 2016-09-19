---
title: "Core.StructAttribute Class (F#)"
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
  - Core.StructAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8a85f5ba-4ea8-438f-b88b-5b0c8b57d018
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.StructAttribute Class (F#)
Adding this attribute to a type causes it to be represented using a .NET Framework structure.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Struct, AllowMultiple = false)>]  
[<Sealed>]  
type StructAttribute =  
 class  
  new StructAttribute : unit -> StructAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `Struct`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.StructAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)   
 [Structures (F#)](../vs140/Structures--F#-.md)