---
title: "Core.ExperimentalAttribute Class (F#)"
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
  - Core.ExperimentalAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: af5fb739-9fce-414d-a956-0ec61326de08
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.ExperimentalAttribute Class (F#)
This attribute is used to tag values that are part of an experimental library feature.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.All, AllowMultiple = false)>]  
[<Sealed>]  
type ExperimentalAttribute =  
 class  
  new ExperimentalAttribute : string -> ExperimentalAttribute  
  member this.Message :  string  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `Experimental`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.ExperimentalAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Message](../vs140/ExperimentalAttribute.Message-Property--F#-.md)|Indicates the warning message to be emitted when F# source code uses this construct.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)