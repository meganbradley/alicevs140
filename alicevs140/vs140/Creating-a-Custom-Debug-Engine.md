---
title: "Creating a Custom Debug Engine"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 52794238-6fae-451c-bf1c-99f344c6f173
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Creating a Custom Debug Engine
A debug engine (DE) is a component that allows debugging of particular run-time architectures. There is typically only one DE implementation per run-time environment.  
  
> [!NOTE]
>  While there are separate DE implementations for Transact-SQL and JScript, VBScript and JScript share a single DE.  
  
 A DE works with the interpreter or operation system to provide such debugging services as execution control, breakpoints, and expression evaluation. These services are implemented through the DE interfaces and can cause the debugger to transition between different operational modes. For more information, see [Operational Modes](../vs140/Operational-Modes.md).  
  
 Creating a DE consists of the following steps:  
  
1.  Registering a DE with Visual Studio  
  
2.  Enabling a program to be debugged  
  
3.  Execution control and state evaluation  
  
4.  Sending events  
  
5.  Termination and detaching  
  
## In This Section  
 [Registering a Custom Debug Engine](../vs140/Registering-a-Custom-Debug-Engine.md)  
 Explains the steps needed to register a debug engine with Visual Studio so that it can be used.  
  
 [Enabling a Program to Be Debugged](../vs140/Enabling-a-Program-to-Be-Debugged.md)  
 Explains that before your DE can debug a program, you must first launch the DE or attach it to an existing program.  
  
 [Execution Control and State Evaluation](../vs140/Execution-Control-and-State-Evaluation.md)  
 Discusses why debugging an application requires implementing execution control features.  
  
 [Sending Events](../vs140/Sending-Events.md)  
 Describes communication between the debugger and the DE as an event model based on DCOM.  
  
 [Termination and Detaching](../vs140/Termination-and-Detaching.md)  
 Explains how to achieve normal termination, which means that there are no breakpoints, exceptions, run-time errors, or infinite loops in the application to be debugged.  
  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)  
 Documents the calling order of the events occurring in a debugging session.  
  
 [How To: Debug a Custom Debug Engine](../Topic/How%20To:%20Debug%20a%20Custom%20Debug%20Engine.md)  
 Explains how to debug a custom DE.  
  
## See Also  
 [Visual Studio Debugging SDK](../vs140/Visual-Studio-Debugger-Extensibility.md)