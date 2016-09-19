---
title: "Core.DefaultAugmentationAttribute Class (F#)"
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
  - Core.DefaultAugmentationAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: add853d3-c839-4720-a6d1-b9dbe5b9db56
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.DefaultAugmentationAttribute Class (F#)
Adding this attribute to a discriminated union with value `false` turns off the generation of standard helper member tester, constructor and accessor members for the generated Common Language Infrastructure (CLI) class for that type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class, AllowMultiple = false)>]  
[<Sealed>]  
type DefaultAugmentationAttribute =  
 class  
  new DefaultAugmentationAttribute : bool -> DefaultAugmentationAttribute  
  member this.Value :  bool  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `DefaultAugmentation`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.DefaultAugmentationAttribute-Constructor--F#-.md)|Creates an instance of the attribute|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Value](../vs140/DefaultAugmentationAttribute.Value-Property--F#-.md)|The value of the attribute, indicating whether the type has a default augmentation or not|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)