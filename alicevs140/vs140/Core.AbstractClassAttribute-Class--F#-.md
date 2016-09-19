---
title: "Core.AbstractClassAttribute Class (F#)"
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
  - Core.AbstractClassAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: dfdc0c97-e72d-4cda-8f3b-7591820e7c44
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.AbstractClassAttribute Class (F#)
Adding this attribute to class definition makes it abstract, which means it need not implement all its methods. Instances of abstract classes may not be constructed directly.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type AbstractClassAttribute =  
 class  
  new AbstractClassAttribute : unit -> AbstractClassAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `AbstractClass`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.AbstractClassAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)