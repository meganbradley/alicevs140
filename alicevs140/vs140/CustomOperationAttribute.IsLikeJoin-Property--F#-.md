---
title: "CustomOperationAttribute.IsLikeJoin Property (F#)"
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
ms.assetid: fac774ad-967c-4513-9388-d58b05f5d453
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CustomOperationAttribute.IsLikeJoin Property (F#)
Indicates if the custom operation is an operation similar to a join in a sequence computation, in that it supports two inputs and a correlation constraint.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Core  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signatures:member this.IsLikeJoin : bool with get, set// Usage:customOperationAttribute.IsLikeJoincustomOperationAttribute.IsLikeJoin <- isLikeJoin  
```  
  
## Property Value  
 `true` if the operation is like a join.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Core.CustomOperationAttribute Class (F#)](../vs140/Core.CustomOperationAttribute-Class--F#-.md)   
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)