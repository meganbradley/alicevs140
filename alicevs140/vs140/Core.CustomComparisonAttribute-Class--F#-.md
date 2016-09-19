---
title: "Core.CustomComparisonAttribute Class (F#)"
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
  - Core.CustomComparisonAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: e25c43cc-e553-44b2-8229-cff53f4af552
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.CustomComparisonAttribute Class (F#)
Adding this attribute to a type indicates it is a type with a user-defined implementation of comparison.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class ||| AttributeTargets.Struct, AllowMultiple = false)>]  
[<Sealed>]  
type CustomComparisonAttribute =  
 class  
  new CustomComparisonAttribute : unit -> CustomComparisonAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `CustomComparison`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.CustomComparisonAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)