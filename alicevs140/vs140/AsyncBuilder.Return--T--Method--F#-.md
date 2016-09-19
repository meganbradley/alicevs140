---
title: "AsyncBuilder.Return&lt;&#39;T&gt; Method (F#)"
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
  - AsyncBuilder.Return<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 0f90f7c3-0774-4557-8d2d-59fe70bd09ea
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBuilder.Return&lt;&#39;T&gt; Method (F#)
Implements the `return` expression in asynchronous computations. Creates an asynchronous computation that returns a result.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Return : 'T -> Async<'T>  
  
// Usage:  
asyncBuilder.Return (value)  
```  
  
#### Parameters  
 `value`  
 Type: `'T`  
  
 The value to return from the computation.  
  
## Return Value  
 An asynchronous computation ([Async](../Topic/Control.Async%20Class%20\(F%23\).md) object) that returns `value` when executed.  
  
## Remarks  
 A cancellation check is performed when the computation is executed. The existence of this method permits the use of `return` in the `async { ... }` computation expression syntax.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.AsyncBuilder Class (F#)](../vs140/Control.AsyncBuilder-Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)