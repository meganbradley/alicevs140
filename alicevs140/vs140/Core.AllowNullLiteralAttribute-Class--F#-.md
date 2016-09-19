---
title: "Core.AllowNullLiteralAttribute Class (F#)"
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
  - Core.AllowNullLiteralAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 4f315196-f444-4cca-ba07-1176ff71eb0f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.AllowNullLiteralAttribute Class (F#)
Adding this attribute to a type lets the `null` literal be used for the type within F# code. This attribute may only be added to F#-defined class or interface types.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type AllowNullLiteralAttribute =  
 class  
  new AllowNullLiteralAttribute : unit -> AllowNullLiteralAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `AllowNullLiteral`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.AllowNullLiteralAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)