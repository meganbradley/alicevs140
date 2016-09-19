---
title: "Microsoft.FSharp.Control Namespace (F#)"
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
  - Microsoft.FSharp.Control
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8dc8478e-41dd-4abc-9f9c-27171f1d25df
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft.FSharp.Control Namespace (F#)
This namespace contains several types that common scenarios in F# programs, including asynchronous programming, message passing, and event-based programming.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Control  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
namespace Microsoft.FSharp.Control  
```  
  
## Remarks  
  
## Modules  
  
|Module|Description|  
|------------|-----------------|  
|module [CommonExtensions](../Topic/Control.CommonExtensions%20Module%20\(F%23\).md)|A module of extension members providing asynchronous operations for some basic CLI types related to concurrency and I/O.|  
|module [Event](../vs140/Control.Event-Module--F#-.md)|Provides functions for managing event streams.|  
|module [LazyExtensions](../vs140/Control.LazyExtensions-Module--F#-.md)|Extensions related to Lazy values.|  
|module [Observable](../vs140/Control.Observable-Module--F#-.md)|Basic operations on first class event and other observable objects.|  
|module [WebExtensions](../vs140/Control.WebExtensions-Module--F#-.md)|A module of extension members providing asynchronous operations for some basic Web operations.|  
  
## Type Definitions  
  
|Type|Description|  
|----------|-----------------|  
|type [Async<'T>](../Topic/Control.Async%3C'T%3E%20Type%20\(F%23\).md)|A compositional asynchronous computation, which, when run, will eventually produce a value of type T, or else raises an exception.|  
|type [Async](../Topic/Control.Async%20Class%20\(F%23\).md)|This static class holds members for creating and manipulating asynchronous computations.|  
|type [AsyncBuilder](../vs140/Control.AsyncBuilder-Class--F#-.md)|The type of the `async` operator, used to build workflows for asynchronous computations.|  
|type [AsyncReplyChannel<'Reply>](../vs140/Control.AsyncReplyChannel--Reply--Class--F#-.md)|A handle to a capability to reply to a PostAndReply message.|  
|type [DelegateEvent<'Delegate>](../vs140/Control.DelegateEvent--Delegate--Class--F#-.md)|Event implementations for an arbitrary type of delegate.|  
|type [Event<'Delegate,'Args>](../vs140/Control.Event--Delegate--Args--Class--F#-.md)|Event implementations for a delegate types following the standard .NET Framework convention of a first 'sender' argument.|  
|type [Event<'T>](../vs140/Control.Event--T--Class--F#-.md)|Event implementations for the IEvent<_> type.|  
|type [Handler<'T>](../vs140/Control.Handler--T--Class--F#-.md)|A delegate type associated with the F# event type `IEvent<_>`|  
|type [IDelegateEvent<'Delegate>](../vs140/Control.IDelegateEvent--Delegate--Interface--F#-.md)|First class event values for arbitrary delegate types.|  
|type [IEvent<'Delegate,'Args>](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)|First class event values for CLI events conforming to CLI Framework standards.|  
|type [MailboxProcessor<'Msg>](../vs140/Control.MailboxProcessor--Msg--Class--F#-.md)|A message-processing agent which executes an asynchronous computation.|  
  
## Type Abbreviations  
  
|Type|Description|  
|----------|-----------------|  
|type [IEvent<'T>](../vs140/Control.IEvent--T--Type-Abbreviation--F#-.md)|First-class listening points (i.e. objects that permit you to register a callback activated when the event is triggered).|  
|type [lazy<'T>](../vs140/Control.lazy--T--Type-Abbreviation.md)|An abbreviation for the type of delayed computations.|  
|type [Lazy<'T>](../vs140/Control.Lazy--T--Type-Abbreviation--F#-.md)|An abbreviation for the type of delayed computations.|  
  
## See Also  
 [F# Library Reference](../Topic/F%23%20Core%20Library%20Reference.md)