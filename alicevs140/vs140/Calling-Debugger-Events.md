---
title: "Calling Debugger Events"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b3440ac3-80af-40c6-bef4-cbf00fa67885
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Calling Debugger Events
Events in debugging sessions occur in a specific order.  
  
## Discussion  
 To understand the pattern of calls between the debug engine (DE) and the session debug manager (SDM), the following represents the calling order of the events that occur in a typical debugging session:  
  
1.  [Attaching and detaching to a program](../vs140/Attaching-and-Detaching-to-a-Program.md)  
  
2.  [Launching the debugger](../vs140/Launching-the-Debugger.md)  
  
3.  [Terminating a program](../vs140/Terminating-a-Program.md)  
  
4.  [Creating a breakpoint](../vs140/Creating-a-Breakpoint.md)  
  
5.  [When a breakpoint binds or becoming unbound](../vs140/When-a-Breakpoint-Binds-or-Becomes-Unbound.md)  
  
6.  [Breakpoint errors](../vs140/Breakpoint-Errors.md)  
  
7.  [Hitting a breakpoint](../vs140/Hitting-a-Breakpoint.md)  
  
8.  [Deleting a breakpoint](../vs140/Deleting-a-Breakpoint.md)  
  
9. [Entering break mode](../vs140/Entering-Break-Mode.md)  
  
10. [Stepping in break mode](../vs140/Stepping-in-Break-Mode.md)  
  
11. [Expression evaluation in break mode](../vs140/Expression-Evaluation-in-Break-Mode.md)  
  
12. [Exception handling](../vs140/Exception-Handling--Visual-Studio-SDK-.md)  
  
## See Also  
 [Creating a Custom Debug Engine](../vs140/Creating-a-Custom-Debug-Engine.md)