---
title: "Core.LiteralAttribute Class (F#)"
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
  - Core.LiteralAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 465f36ce-d146-41c0-b425-679c509cd285
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.LiteralAttribute Class (F#)
Adding this attribute to a value causes it to be compiled as a .NET Framework constant literal.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Field, AllowMultiple = false)>]  
[<Sealed>]  
type LiteralAttribute =  
 class  
  new LiteralAttribute : unit -> LiteralAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `Literal`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.LiteralAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)