---
title: "Sending Events"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 064231e7-59b5-4437-8240-a23c0a7ec2a9
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Sending Events
The mechanism for communication between the debugger and the debug engine (DE) is an event model based on DCOM. Events are sent as COM objects, and each event has parameters that specify the following:  
  
-   The DE that called the event.  
  
-   A description of what happened.  
  
-   The process, program, and thread information that identifies the context of where the event occurred. The process is not sent for events sent from a DE.  
  
-   The event type that indicates whether the event is synchronous or asynchronous.  
  
 All debug events are sent using the method [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md).  
  
## In This Section  
 [Event Sources](../vs140/Event-Sources--Visual-Studio-SDK-.md)  
 Explains the two sources of events: the debug engine (DE) and the session debug manager (SDM).  
  
 [Supported Event Types](../vs140/Supported-Event-Types.md)  
 Discusses the currently supported event types: asynchronous and synchronous.  
  
 [Event Descriptions](../vs140/Event-Descriptions.md)  
 Defines events and the reasons for their use.  
  
## Related Sections  
 [Creating a Custom Debug Engine](../vs140/Creating-a-Custom-Debug-Engine.md)  
 Describes how a DE works with the interpreter or operating system to provide debugging services.