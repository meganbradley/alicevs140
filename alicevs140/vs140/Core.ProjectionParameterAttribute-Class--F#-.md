---
title: "Core.ProjectionParameterAttribute Class (F#)"
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
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: b71b8ac1-0fd4-41d2-b97e-d6fc118421fa
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.ProjectionParameterAttribute Class (F#)
Indicates that, when a custom operator is used in a computation expression, a parameter is automatically parameterized by the variable space of the computation expression.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Parameter, AllowMultiple = false)>][<Sealed>type ProjectionParameterAttribute =  class     new ProjectionParameterAttribute : unit -> ProjectionParameterAttribute end  
```  
  
## Remarks  
 You can also use the short form of the name, `ProjectionParameter`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.ProjectionParameterAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)