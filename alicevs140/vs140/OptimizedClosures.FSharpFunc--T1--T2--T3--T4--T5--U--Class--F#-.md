---
title: "OptimizedClosures.FSharpFunc&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4,&#39;T5,&#39;U&gt; Class (F#)"
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
  - OptimizedClosures.FSharpFunc<'T1,'T2,'T3,'T4,'T5,'U>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 797270e8-2a37-495c-9b4b-48292415d213
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OptimizedClosures.FSharpFunc&lt;&#39;T1,&#39;T2,&#39;T3,&#39;T4,&#39;T5,&#39;U&gt; Class (F#)
The .NET Framework type used to represent F# function values that accept five curried arguments without intervening execution. This type should not typically used directly from either F# code or from other .NET Framework languages.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Core.OptimizedClosures  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<AbstractClass>]  
type FSharpFunc<'T1,'T2,'T3,'T4,'T5,'U> =  
 class  
  new FSharpFunc : unit -> FSharpFunc<'T1,'T2,'T3,'T4,'T5,'U>  
  static member FSharpFunc.Adapt : ('T1 -> 'T2 -> 'T3 -> 'T4 -> 'T5 -> 'U) -> FSharpFunc<'T1,'T2,'T3,'T4,'T5,'U>  
  abstract this.Invoke : FSharpFunc<'T1,'T2,'T3,'T4,'T5,'U> -> 'T1 * 'T2 * 'T3 * 'T4 * 'T5 -> 'U  
 end  
```  
  
## Remarks  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/OptimizedClosures.FSharpFunc--T1--T2--T3--T4--T5--U--Constructor--F#-.md)|Construct an optimized function value that can accept five curried arguments without intervening execution.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Invoke](../vs140/FSharpFunc.Invoke--T1--T2--T3--T4--T5--U--Method--F#-.md)|Invoke an F# first class function value that accepts five curried arguments without intervening execution|  
  
## Static Members  
  
|Member|Description|  
|------------|-----------------|  
|[Adapt](../vs140/FSharpFunc.Adapt--T1--T2--T3--T4--T5--U--Method--F#-.md)|Adapt an F# first class function value to be an optimized function value that can accept five curried arguments without intervening execution.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Core.OptimizedClosures Namespace (F#)](../vs140/Core.OptimizedClosures-Module--F#-.md)