---
title: "Async.AwaitEvent&lt;&#39;Del,&#39;T&gt; Method (F#)"
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
  - Async.AwaitEvent<'Del,'T>
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 08457e9a-0c8e-4ade-9146-3dbe10c28584
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Async.AwaitEvent&lt;&#39;Del,&#39;T&gt; Method (F#)
Creates an asynchronous computation that waits for a single invocation of a CLI event by adding a handler to the event. Once the computation completes or is cancelled, the handler is removed from the event.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
static member AwaitEvent : IEvent<'Del,'T> * ?(unit -> unit) -> Async<'T> (requires delegate)  
  
// Usage:  
Async.AwaitEvent (event)  
Async.AwaitEvent (event, cancelAction = cancelAction)  
```  
  
#### Parameters  
 `event`  
 Type: [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)`<'Del,'T>`  
  
 The event to handle once.  
  
 `cancelAction`  
 Type: `(`[unit](../vs140/Core.unit-Type-Abbreviation--F#-.md) `->` [unit](../vs140/Core.unit-Type-Abbreviation--F#-.md)`)`  
  
 An optional function to execute instead of cancelling when a cancellation is issued.  
  
## Return Value  
 An asynchronous computation that waits for the event to be invoked.  
  
## Remarks  
 The computation will respond to cancellation while waiting for the event. If a cancellation occurs, and `cancelAction` is specified, then it is executed, and the computation continues to wait for the event. If `cancelAction` is not specified, then cancellation causes the computation to cancel immediately.  
  
## Example  
 The following code example demonstrates how to use `Async.AwaitEvent` to set up a file operation that runs in response to an event that indicates that a file is changed. In this case, waiting for the event prevents an attempt to access the file while it is locked.  
  
 [!CODE [FsAsyncAPIs#14](../CodeSnippet/VS_Snippets_Fsharp/fsasyncapis#14)]  
  
 **Sample Output**  
  
  **Creating file Waiting for file sylongoutput.dat.**  
**stem watcher notification.**  
**Attempting to write to file longoutput.dat.**  
**The file longoutput.dat is changed.**  
**The file longoutput.dat is changed.**  
**Attempting to open and read file longoutput.dat.**  
**Successfully read file longoutput.dat.**   
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Control.Async Class (F#)](../Topic/Control.Async%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)