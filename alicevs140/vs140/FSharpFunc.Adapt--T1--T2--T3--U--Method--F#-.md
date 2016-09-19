---
title: "FSharpFunc.Adapt&lt;&#39;T1,&#39;T2,&#39;T3,&#39;U&gt; Method (F#)"
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
  - FSharpFunc.Adapt<'T1,'T2,'T3,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 785cfdb2-21e1-4f8f-930f-db6de480ae47
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FSharpFunc.Adapt&lt;&#39;T1,&#39;T2,&#39;T3,&#39;U&gt; Method (F#)
Adapt an F# first class function value to be an optimized function value that can accept three curried arguments without intervening execution.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.OptimizedClosures  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member FSharpFunc.Adapt : ('T1 -> 'T2 -> 'T3 -> 'U) -> FSharpFunc<'T1,'T2,'T3,'U>  
  
// Usage:  
FSharpFunc.Adapt (func)  
```  
  
#### Parameters  
 `func`  
 Type: `'T1 -> 'T2 -> 'T3 -> 'U`  
  
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
 [OptimizedClosures.FSharpFunc<'T1,'T2,'T3,'U> Class (F#)](../vs140/OptimizedClosures.FSharpFunc--T1--T2--T3--U--Class--F#-.md)   
 [Microsoft.FSharp.Core.OptimizedClosures Namespace (F#)](../vs140/Core.OptimizedClosures-Module--F#-.md)