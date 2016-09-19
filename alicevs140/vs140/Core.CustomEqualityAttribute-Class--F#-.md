---
title: "Core.CustomEqualityAttribute Class (F#)"
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
  - Core.CustomEqualityAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 798e06a2-fbc1-452c-a606-5f050227866e
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.CustomEqualityAttribute Class (F#)
Indicates that a type has a user-defined implementation of equality.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class ||| AttributeTargets.Struct, AllowMultiple = false)>]  
[<Sealed>]  
type CustomEqualityAttribute =  
 class  
  new CustomEqualityAttribute : unit -> CustomEqualityAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `CustomEquality`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.CustomEqualityAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)