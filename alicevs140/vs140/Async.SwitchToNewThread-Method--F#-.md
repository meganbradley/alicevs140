---
title: "Async.SwitchToNewThread Method (F#)"
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
  - Async.SwitchToNewThread
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 1f0b78f7-8621-47da-89e8-5040ead1004c
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.SwitchToNewThread Method (F#)
Creates an asynchronous computation that creates a new thread and runs its continuation in that thread.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member SwitchToNewThread : unit -> Async<unit>  
  
// Usage:  
Async.SwitchToNewThread ()  
```  
  
## Return Value  
 A computation that will execute on a new thread.  
  
## Remarks  
  
## Example  
 The following code example shows how to use `Async.SwitchToNewThread` and [Async.SwitchToThreadPool](../vs140/Async.SwitchToThreadPool-Method--F#-.md) to wrap a synchronous method call as an asynchronous method.  
  
 [!CODE [FsAsyncAPIs#28](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#28)]  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)