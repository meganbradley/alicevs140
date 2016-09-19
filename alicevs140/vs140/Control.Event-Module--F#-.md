---
title: "Control.Event Module (F#)"
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
  - Control.Event
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 8b883baa-a460-4840-9baa-de8260351bc7
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Control.Event Module (F#)
Provides functions for managing event streams.  
  
 **Namespace/Module Path:** Microsoft.FSharp.Control  
  
 **Assembly:** FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
module Event  
```  
  
## Remarks  
  
## Values  
  
|Value|Description|  
|-----------|-----------------|  
|[add](../vs140/Event.add--T--Del--Function--F#-.md)  `: ('T -> unit) -> Event<'Del,'T> -> unit`|Runs the given function each time the given event is triggered.|  
|[choose](../vs140/Event.choose--T--U--Del--Function--F#-.md)  `: ('T -> 'U option) -> IEvent<'Del,'T> -> IEvent<'U>`|Returns a new event which fires on a selection of messages from the original event. The selection function takes an original message to an optional new message.|  
|[filter](../vs140/Event.filter--T--Del--Function--F#-.md)  `: ('T -> bool) -> IEvent<'Del,'T> -> IEvent<'T>`|Returns a new event that listens to the original event and triggers the resulting event only when the argument to the event passes the given function.|  
|[map](../vs140/Event.map--T--U--Del--Function--F#-.md)  `: ('T -> 'U) -> IEvent<'Del, 'T> -> IEvent<'U>`|Returns a new event that passes values transformed by the given function.|  
|[merge](../vs140/Event.merge--Del1--T--Del2--Function--F#-.md)  `: IEvent<'Del1,'T> -> IEvent<'Del2,'T> -> IEvent<'T>`|Fires the output event when either of the input events fire.|  
|[pairwise](../vs140/Event.pairwise--Del--T--Function--F#-.md)  `: IEvent<'Del,'T> -> IEvent<'T * 'T>`|Returns a new event that triggers on the second and subsequent triggerings of the input event. The Nth triggering of the input event passes the arguments from the N-1th and Nth triggering as a pair. The argument passed to the N-1th triggering is held in hidden internal state until the Nth triggering occurs.|  
|[partition](../vs140/Event.partition--T--Del--Function--F#-.md)  `: ('T -> bool) -> IEvent<'Del,'T> -> IEvent<'T> * IEvent<'T>`|Returns a new event that listens to the original event and triggers the first resulting event if the application of the predicate to the event arguments returned `true`, and the second event if it returned `false`.|  
|[scan](../vs140/Event.scan--U--T--Del--Function--F#-.md)  `: ('U -> 'T -> 'U) -> 'U -> IEvent<'Del,'T> -> IEvent<'U>`|Returns a new event consisting of the results of applying the given accumulating function to successive values triggered on the input event. An item of internal state records the current value of the state parameter. The internal state is not locked during the execution of the accumulation function, so care should be taken that the input [IEvent](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md) not triggered by multiple threads simultaneously.|  
|[split](../vs140/Event.split--T--U1--U2--Del--Function--F#-.md)  `: ('T -> Choice<'U1,'U2>) -> IEvent<'Del,'T> -> IEvent<'U1> * IEvent<'U2>`|Returns a new event that listens to the original event and triggers the first resulting event if the application of the function to the event arguments returned a `Choice1Of2`, and the second event if it returns a `Choice2Of2`.|  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 2.0, 4.0, Portable  
  
## See Also  
 [Microsoft.FSharp.Control Namespace (F#)](../vs140/Microsoft.FSharp.Control-Namespace--F#-.md)   
 [Event Class](../vs140/Control.Event--T--Class--F#-.md)   
 [Events (F#)](../Topic/Events%20\(F%23\).md)   
 [IEvent Interface](../vs140/Control.IEvent--Delegate--Args--Interface--F#-.md)