---
title: "Enabling a Program to Be Debugged"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61d24820-0cd9-48b6-8674-6813f7493237
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Enabling a Program to Be Debugged
Before your debug engine (DE) can debug a program, you must first launch the DE or attach it to an existing program.  
  
## In This Section  
 [Getting a Port](../vs140/Getting-a-Port.md)  
 Discusses how to obtain a port as the first step to enabling a program to be debugged.  
  
 [Registering the Program](../vs140/Registering-the-Program.md)  
 Explains the next step in enabling a program to be debugged: registering it with the port. Once registered, the program can be debugged either by the process of attaching or just-in-time (JIT) debugging.  
  
 [Attaching to the Program](../vs140/Attaching-to-the-Program.md)  
 Explains the next step:attaching the debugger to the program.  
  
 [Launch-based Attaching](../vs140/Launch-based-Attachment.md)  
 Describes launch-based attachment to a program, which is automatic upon launch by the SDM.  
  
 [Sending the Required Events](../vs140/Sending-the-Required-Events.md)  
 Steps you through the required events when creating a debug engine (DE) and attaching it to a program.  
  
## Related Sections  
 [Creating a Custom Debug Engine](../vs140/Creating-a-Custom-Debug-Engine.md)  
 Defines a debug engine (DE), and describes services implemented through the DE interfaces and how they can cause the debugger to transition between different operational modes.