---
title: "Async.StartImmediate Method (F#)"
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
ms.assetid: 2f71d1cc-187f-48cf-ac66-e7fda41c46e3
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.StartImmediate Method (F#)
Runs an asynchronous computation, starting immediately on the current operating system thread.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member StartImmediate : Async<unit> * CancellationToken option -> unit  
  
// Usage:  
Async.StartImmediate (computation)  
Async.StartImmediate (computation, cancellationToken = cancellationToken)  
```  
  
#### Parameters  
 `computation`  
 Type: [Async](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)`<`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`>`  
  
 The asynchronous computation to execute.  
  
 `cancellationToken`  
 Type: [CancellationToken](../Topic/Threading.CancellationToken%20Structure%20\(F%23\).md)  
  
 The optional cancellation token to associate with the computation. The default is used if this parameter is not provided.  
  
## Remarks  
 If no cancellation token is provided then the default cancellation token is used.  
  
## Example  
 The following code example shows how to use `Async.StartImmediate` to start an asynchronous computation on the current thread. Often, an asynchronous operation needs to update UI, which should always be done on the UI thread. When your asynchronous operation needs to begin by updating UI, `Async.StartImmediate` is a better choice than [Async.Start](../vs140/Async.Start-Method--F#-.md), which starts the asynchronous operation on a thread pool thread.  
  
 [!CODE [FsAsyncAPIs#320](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#320)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)