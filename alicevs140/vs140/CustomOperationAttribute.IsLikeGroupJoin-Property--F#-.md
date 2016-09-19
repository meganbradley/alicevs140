---
title: "CustomOperationAttribute.IsLikeGroupJoin Property (F#)"
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
ms.assetid: 81cecf4a-54d4-419c-81d2-3a04337b6952
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CustomOperationAttribute.IsLikeGroupJoin Property (F#)
Indicates if the custom operation is an operation similar to a group join in a sequence computation, in that the operation supports two inputs and a correlation constraint, and generates a group.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:member this.IsLikeGroupJoin : bool with get, set// Usage:customOperationAttribute.IsLikeGroupJoincustomOperationAttribute.IsLikeGroupJoin <- isLikeGroupJoin  
```  
  
## Property Value  
 `true` if the operation resembles a group join.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.CustomOperationAttribute Class (F#)](../vs140/Core.CustomOperationAttribute-Class--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)