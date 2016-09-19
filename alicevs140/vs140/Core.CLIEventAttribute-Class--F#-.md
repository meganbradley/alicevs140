---
title: "Core.CLIEventAttribute Class (F#)"
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
  - Core.CLIEventAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: d359f1dd-ffa5-42fb-8808-b4c8131a0333
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.CLIEventAttribute Class (F#)
Adding this attribute to a property with event type causes it to be compiled with as a Common Language Infrastructure (CLI) metadata event, through a syntactic translation to a pair of `add_EventName` and `remove_EventName` methods.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Property, AllowMultiple = false)>]  
[<Sealed>]  
type CLIEventAttribute =  
 class  
  new CLIEventAttribute : unit -> CLIEventAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `CLIEvent`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.CLIEventAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)