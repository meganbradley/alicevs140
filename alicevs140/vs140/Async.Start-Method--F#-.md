---
title: "Async.Start Method (F#)"
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
  - Async.Start
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 338aa756-beac-4dc1-95ca-613822679347
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.Start Method (F#)
Starts the asynchronous computation in the thread pool. Do not await its result.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member Start : Async<unit> * ?CancellationToken -> unit  
  
// Usage:  
Async.Start (computation)  
Async.Start (computation, cancellationToken = cancellationToken)  
```  
  
#### Parameters  
 `computation`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`>`  
  
 The computation to run asynchronously.  
  
 `cancellationToken`  
 Type: [CancellationToken](../Topic/Threading.CancellationToken%20Structure%20\(F%23\).md)  
  
 The cancellation token to be associated with the computation. If one is not supplied, the default cancellation token is used.  
  
## Remarks  
 If no cancellation token is provided then the default cancellation token is used.  
  
## Example  
 The following code example shows how to start an asynchronous computation on the thread pool.  
  
 [!CODE [FsAsyncAPIs#31](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#31)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)