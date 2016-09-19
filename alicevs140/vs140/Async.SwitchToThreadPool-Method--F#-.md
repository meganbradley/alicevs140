---
title: "Async.SwitchToThreadPool Method (F#)"
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
  - Async.SwitchToThreadPool
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: c2708739-5389-487a-a3c9-490f417bcdc6
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.SwitchToThreadPool Method (F#)
Creates an asynchronous computation that queues a work item that runs its continuation.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member SwitchToThreadPool : unit -> Async<unit>  
  
// Usage:  
Async.SwitchToThreadPool ()  
```  
  
## Return Value  
 A computation that generates a new work item in the thread pool.  
  
## Remarks  
 For examples of the use of this method, see [Async.SwitchToContext](../Topic/Async.SwitchToContext%20Method%20\(F%23\).md) and [Async.SwitchToNewThread](../vs140/Async.SwitchToNewThread-Method--F#-.md).  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)