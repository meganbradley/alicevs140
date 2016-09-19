---
title: "Core.NoComparisonAttribute Class (F#)"
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
  - Core.NoComparisonAttribute
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 2203a119-7e12-48cc-9b8d-58d07db3da26
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.NoComparisonAttribute Class (F#)
Adding this attribute to a type indicates it is a type where comparison is an abnormal operation. This means that the type does not satisfy the F# comparison constraint. Within the bounds of the F# type system, this helps ensure that the F# generic comparison function is not instantiated directly at this type. The attribute and checking does not constrain the use of comparison with base or child types of this type.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AttributeUsage(AttributeTargets.Class ||| AttributeTargets.Interface ||| AttributeTargets.Delegate ||| AttributeTargets.Struct ||| AttributeTargets.Enum, AllowMultiple = false)>]  
[<Sealed>]  
type NoComparisonAttribute =  
 class  
  new NoComparisonAttribute : unit -> NoComparisonAttribute  
 end  
```  
  
## Remarks  
 You can also use the short form of the name, `NoComparison`.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Core.NoComparisonAttribute-Constructor--F#-.md)|Creates an instance of the attribute.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)