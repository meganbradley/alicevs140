---
title: "Attaching Directly to a Program"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ad2b7db8-821c-440c-ba07-c55c6a395e0f
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Attaching Directly to a Program
Users who want to debug programs in a process that is already running typically follow this process:  
  
1.  In the IDE, choose the **Debug Processes** command from the **Tools** menu.  
  
     The **Processes** dialog box appears.  
  
2.  Choose a process and click the **Attach** button.  
  
     The **Attach to Process** dialog box appears, listing all debug engines (DEs) installed on the machine.  
  
3.  Specify the DEs to use to debug the selected process, and then click **OK**.  
  
 The debug package starts a debug session and passes the list of DEs to it. The debug session in turn passes this list, along with a callback function, to the selected process, and then asks the process to enumerate its running programs.  
  
 Programmatically, in response to the user request, the debug package instantiates the session debug manager (SDM) and passes the list of selected DEs to it. Along with the list, the debug package passes the SDM an [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) interface. The debug package passes the list of DEs to the selected process by calling [IDebugProcess2::Attach](../vs140/IDebugProcess2--Attach.md). The SDM then calls [IDebugProcess2::EnumPrograms](../vs140/IDebugProcess2--EnumPrograms.md) on the port to enumerate the programs running in the process.  
  
 From this point on, each debug engine is attached to a program exactly as detailed in [Attaching After a Launch](../vs140/Attaching-After-a-Launch.md), with two exceptions.  
  
 For efficiency, DEs that are implemented to share an address space with the SDM are grouped so that each DE has a set of programs it will attach to. In this case, [IDebugProcess2](../vs140/IDebugProcess2.md) calls [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) and passes it an array of programs to attach to.  
  
 The second exception is that the startup events sent by a DE attaching to a program that is already running do not typically include the entry point event.  
  
## See Also  
 [Sending Startup Events After a Launch](../vs140/Sending-Startup-Events-After-a-Launch.md)   
 [Debugging Tasks](../vs140/Debugging-Tasks.md)