---
title: "Debugging Tasks"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5d60e9e8-305e-4a48-829f-b9440fc8af7b
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Debugging Tasks
To debug a program, it must be launched and a debug engine (DE) must be attached to it, or else the DE must be attached to a previously launched program. Once attached, the DE must generate certain startup events. In response, the debug package attempts to bind the breakpoints set in the IDE. When the program hits a bound breakpoint, it halts and waits for user input.  
  
## In This Section  
 [Security Issues](../vs140/Security-Issues.md)  
 Discusses the security steps that are needed to debug a program.  
  
 [Launching a Program](../Topic/Launching%20a%20Program.md)  
 Provides step-by-step instructions on how to specify a DE, which calls the operating system to launch the program.  
  
 [Attaching Directly to a Program](../vs140/Attaching-Directly-to-a-Program.md)  
 Describes the process used to debug a program in a process that is already running.  
  
 [Sending Startup Events After a Launch](../vs140/Sending-Startup-Events-After-a-Launch.md)  
 Lists the events that take place once the DE is attached to the program, until the program is at its main entry point and is ready for debugging.  
  
 [Control of Execution](../vs140/Control-of-Execution.md)  
 Explains how the DE typically sends an entry-point event, a load-complete event, or a stopping event, depending on the circumstances.  
  
 [Binding Breakpoints](../vs140/Binding-Breakpoints.md)  
 Describes how, if the user sets a breakpoint, the IDE formulates the request and prompts the debug session to create the breakpoint.  
  
 [Evaluating Expressions](../vs140/Evaluating-Expressions.md)  
 Explains how expressions are created and what happens when an expression is evaluated.  
  
 [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md)  
 Explains how type visualizers and custom viewers are supported by the expression evaluator (EE).  
  
## Related Sections  
 [Debugger Concepts](../vs140/Debugger-Concepts.md)  
 Describes the main debugging architectural concepts.  
  
 [Debugger Components](../vs140/Debugger-Components.md)  
 Provides an overview of the Visual Studio debugging components, which include the DE, EE, and symbol handler (SH).  
  
 [Debugger Contexts](../vs140/Debugger-Contexts.md)  
 Explains how the DE operates simultaneously within code, documentation, and expression evaluation contexts. Describes, for each of the three contexts, the location, position, or evaluation relevant to it.  
  
## See Also  
 [Getting Started (Visual Studio Debugging SDK)](../vs140/Getting-Started-with-Debugger-Extensibility.md)