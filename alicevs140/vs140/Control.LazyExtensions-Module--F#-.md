---
title: "Control.LazyExtensions Module (F#)"
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
  - Control.LazyExtensions
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 86671f40-84a0-402a-867d-ae596218d948
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.LazyExtensions Module (F#)
Extensions related to Lazy values.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AutoOpen>]  
module LazyExtensions  
```  
  
## Remarks  
  
## Extension Members  
  
|Extension Member|Description|  
|----------------------|-----------------|  
|[Create](../vs140/Lazy.Create--T--Extension-Method--F#-.md)  `: Lazy<'T>`|Creates a lazy computation that evaluates to the result of the given function when forced.|  
|[CreateFromValue](../vs140/Lazy.CreateFromValue--T--Extension-Method--F#-.md)  `: Lazy<'T>`|Creates a lazy computation that evaluates to the given value when forced.|  
|[Force](../vs140/Lazy.Force--T--Extension-Method--F#-.md)  `: unit -> 'T`|Forces the execution of this value and returns its result. Same as <xref:System.Lazy`1.Value?qualifyHint=False>. Mutual exclusion is used to prevent other threads from also computing the value.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)   
 [Lazy Computations (F#)](../vs140/Lazy-Computations--F#-.md)