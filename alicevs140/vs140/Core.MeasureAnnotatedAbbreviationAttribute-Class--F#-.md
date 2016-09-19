---
title: "Core.MeasureAnnotatedAbbreviationAttribute Class (F#)"
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
  - Core.MeasureAnnotatedAbbreviationAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 11c1a476-9661-40a6-92c8-2e7889f33d88
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.MeasureAnnotatedAbbreviationAttribute Class (F#)
Adding this attribute to a type causes it to be interpreted as a refined type, currently limited to measure-parameterized types. This may only be used under very limited conditions.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type MeasureAnnotatedAbbreviationAttribute =  
 class  
  new MeasureAnnotatedAbbreviationAttribute : unit -> MeasureAnnotatedAbbreviationAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `MeasureAnnotatedAbbreviation`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.MeasureAnnotatedAbbreviationAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)