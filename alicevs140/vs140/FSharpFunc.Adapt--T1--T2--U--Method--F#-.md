---
title: "FSharpFunc.Adapt&lt;&#39;T1,&#39;T2,&#39;U&gt; Method (F#)"
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
  - FSharpFunc.Adapt<'T1,'T2,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 17223c26-7923-4b96-8ee8-3c1ce77fdcf6
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpFunc.Adapt&lt;&#39;T1,&#39;T2,&#39;U&gt; Method (F#)
Adapt an F# first class function value to be an optimized function value that can accept two curried arguments without intervening execution.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.OptimizedClosures  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member FSharpFunc.Adapt : ('T1 -> 'T2 -> 'U) -> FSharpFunc<'T1,'T2,'U>  
  
// Usage:  
FSharpFunc.Adapt (func)  
```  
  
#### Parameters  
 `func`  
 Type: `'T1 -> 'T2 -> 'U`  
  
 The input function.  
  
## Return Value  
 The adapted function.  
  
## Remarks  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [OptimizedClosures.FSharpFunc<'T1,'T2,'U> Class (F#)](../vs140/OptimizedClosures.FSharpFunc--T1--T2--U--Class--F#-.md)   
 [Microsoft.FSharp.Core.OptimizedClosures Namespace (F#)](../vs140/Core.OptimizedClosures-Module--F#-.md)