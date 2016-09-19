---
title: "Core.OptimizedClosures Module (F#)"
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
  - Core.OptimizedClosures
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8f1e5ba0-9ae6-45d5-949a-150fda7eeedb
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Core.OptimizedClosures Module (F#)
An implementation module used to hold some private implementations of function value invocation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module OptimizedClosures  
```  
  
## Remarks  
  
## Type Definitions  
  
|Type|Description|  
|----------|-----------------|  
|type [FSharpFunc<'T1,'T2,'U>](../vs140/OptimizedClosures.FSharpFunc--T1--T2--U--Class--F#-.md)|The .NET Framework type used to represent F# function values that accept two iterated (curried) arguments without intervening execution. This type should not typically used directly from either F# code or from other .NET Framework languages.|  
|type [FSharpFunc<'T1,'T2,'T3,'U>](../vs140/OptimizedClosures.FSharpFunc--T1--T2--T3--U--Class--F#-.md)|The .NET Framework type used to represent F# function values that accept three iterated (curried) arguments without intervening execution. This type should not typically used directly from either F# code or from other .NET Framework languages.|  
|type [FSharpFunc<'T1,'T2,'T3,'T4,'U>](../vs140/OptimizedClosures.FSharpFunc--T1--T2--T3--T4--U--Class--F#-.md)|The .NET Framework type used to represent F# function values that accept four curried arguments without intervening execution. This type should not typically used directly from either F# code or from other .NET Framework languages.|  
|type [FSharpFunc<'T1,'T2,'T3,'T4,'T5,'U>](../vs140/OptimizedClosures.FSharpFunc--T1--T2--T3--T4--T5--U--Class--F#-.md)|The .NET Framework type used to represent F# function values that accept five curried arguments without intervening execution. This type should not typically used directly from either F# code or from other .NET Framework languages.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core Namespace (F#)](../Topic/Microsoft.FSharp.Core%20Namespace%20\(F%23\).md)