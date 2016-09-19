---
title: "Core.MeasureAttribute Class (F#)"
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
  - Core.MeasureAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 553c9d6b-880c-4592-ba0b-756bc9f47a2b
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.MeasureAttribute Class (F#)
Adding this attribute to a type causes it to be interpreted as a unit of measure. This may only be used under very limited conditions.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.GenericParameter ||| AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type MeasureAttribute =  
 class  
  new MeasureAttribute : unit -> MeasureAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `Measure`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.MeasureAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)