---
title: "Control.AsyncBuilder Class (F#)"
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
  - Control.AsyncBuilder
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 7f593fcf-bc6e-42fc-bd26-fb9e18951016
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.AsyncBuilder Class (F#)
The type of the `async` operator, used to build workflows for asynchronous computations.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
[<Sealed>]  
type AsyncBuilder =  
 class  
  new AsyncBuilder : unit -> AsyncBuilder  
  member this.Bind : Async<'T> * ('T -> Async<'U>) -> Async<'U>  
  member this.Combine : Async<unit> * Async<'T> -> Async<'T>  
  member this.Delay : (unit -> Async<'T>) -> Async<'T>  
  member this.For : seq<'T> * ('T -> Async<unit>) -> Async<unit>  
  member this.Return : 'T -> Async<'T>  
  member this.ReturnFrom : Async<'T> -> Async<'T>  
  member this.TryFinally : Async<'T> * (unit -> unit) -> Async<'T>  
  member this.TryWith : Async<'T> * (exn -> Async<'T>) -> Async<'T>  
  member this.Using : 'T * ('T -> Async<'U>) -> Async<'U>  
  member this.While : (unit -> bool) * Async<unit> -> Async<unit>  
  member this.Zero : unit -> Async<unit>  
 end  
```  
  
## Remarks  
 For general information on computation expressions and builder types, see [Computation Expressions (F#)](../Topic/Computation%20Expressions%20\(F%23\).md).  
  
 This type is named `FSharpAsyncBuilder` in compiled assemblies. If accessing the type from a language other than F#, or through reflection, use this name.  
  
## Constructors  
  
|Member|Description|  
|------------|-----------------|  
|[new](../vs140/Control.AsyncBuilder-Constructor--F#-.md)|Generates an object used to build asynchronous computations using F# computation expressions. The value `async` is a pre-defined instance of this type. A cancellation check is performed when the computation is executed.|  
  
## Instance Members  
  
|Member|Description|  
|------------|-----------------|  
|[Bind](../vs140/AsyncBuilder.Bind--T--U--Method--F#-.md)|Implements `let!` in asynchronous computations.|  
|[Combine](../vs140/AsyncBuilder.Combine--T--Method--F#-.md)|Creates an asynchronous computation that first runs `computation1` and then runs `computation2`, returning the result of `computation2`.|  
|[Delay](../vs140/AsyncBuilder.Delay--T--Method--F#-.md)|Creates an asynchronous computation that runs a function.|  
|[For](../vs140/AsyncBuilder.For--T--Method--F#-.md)|Implements the `for` expression in asynchronous computations.|  
|[Return](../vs140/AsyncBuilder.Return--T--Method--F#-.md)|Implements the `return` expression in asynchronous computations. Creates an asynchronous computation that returns the specified result.|  
|[ReturnFrom](../vs140/AsyncBuilder.ReturnFrom--T--Method--F#-.md)|Implements the `return!` keyword for asynchronous computations. This function delegates to the input computation.|  
|[TryFinally](../vs140/AsyncBuilder.TryFinally--T--Method--F#-.md)|Implements `try...finally` in asynchronous computations.|  
|[TryWith](../vs140/AsyncBuilder.TryWith--T--Method--F#-.md)|Implements `try...with` in asynchronous computations.|  
|[Using](../vs140/AsyncBuilder.Using--T--U--Method--F#-.md)|Implements the `use` and `use!` keywords in asynchronous computation expressions.|  
|[While](../vs140/AsyncBuilder.While-Method--F#-.md)|Implements the `while` keyword in asynchronous computation expressions.|  
|[Zero](../vs140/AsyncBuilder.Zero-Method--F#-.md)|Creates an asynchronous computation that does nothing and returns `()`.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)