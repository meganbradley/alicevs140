---
title: "Core.GeneralizableValueAttribute Class (F#)"
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
  - Core.GeneralizableValueAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 80cf5376-ac02-42d2-99d5-e1d662907a32
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.GeneralizableValueAttribute Class (F#)
Adding this attribute to a non-function value with generic parameters indicates that uses of the construct can give rise to generic code through type inference.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Method, AllowMultiple = false)>]  
[<Sealed>]  
type GeneralizableValueAttribute =  
 class  
  new GeneralizableValueAttribute : unit -> GeneralizableValueAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `GeneralizableValue`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.GeneralizableValueAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)