---
title: "Program Nodes"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c5a5c13-c14d-42c3-af11-4c63f1032c8d
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Program Nodes
In terms of the debugger architecture, a **program node**:  
  
-   Is a lightweight description of a program.  
  
-   Can identify itself and the process it is running in, and can be attached to, be detached from, and describe the debug engine (DE) that created it, if any.  
  
-   Is represented by an [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) interface, typically created by a DE or port. Program nodes are added to a port by calling [AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md). When a program node is added to a port, it is added to the process containing the program that this program node represents.  
  
 Sometime after a debug session is started, depending on the implementation of the debug package, program nodes are used to create corresponding programs. When a process is queried for its programs, the programs are enumerated, one for each program node.  
  
 Before a program is attached to, the IDE needs only a lightweight description of the program. This information can be obtained from the program node. Once the program is attached to, the IDE needs to display more detailed information, such as a list of all threads running in the program. This information is obtained from the program itself.  
  
## See Also  
 [Programs](../vs140/Programs.md)   
 [Processes](../vs140/Processes.md)   
 [Debug Engine](../vs140/Debug-Engine.md)   
 [Debugger Concepts](../vs140/Debugger-Concepts.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md)