---
title: "AsyncBuilder.Combine&lt;&#39;T&gt; Method (F#)"
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
  - AsyncBuilder.Combine<'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 26ffe7f2-31e3-475f-9042-94347187b721
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AsyncBuilder.Combine&lt;&#39;T&gt; Method (F#)
Creates an asynchronous computation that first runs one computation and then runs another computation, returning the result of the second computation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Combine : Async<unit> * Async<'T> -> Async<'T>  
  
// Usage:  
asyncBuilder.Combine (computation1, computation2)  
```  
  
#### Parameters  
 `computation1`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`>`  
  
 The first part of the sequenced computation.  
  
 `computation2`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<'T>`  
  
 The second part of the sequenced computation.  
  
## Return Value  
 An asynchronous computation that runs both of the computations sequentially.  
  
## Remarks  
 A cancellation check is performed when the computation is executed. The existence of this method permits the use of expression sequencing in the `async { ... }` computation expression syntax.  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.AsyncBuilder Class (F#)](../vs140/Control.AsyncBuilder-Class--F#-.md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)