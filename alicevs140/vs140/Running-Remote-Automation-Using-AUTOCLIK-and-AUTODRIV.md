---
title: "Running Remote Automation Using AUTOCLIK and AUTODRIV"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8900c0de-8dba-4f0a-8d9e-7db77a1f4f46
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Running Remote Automation Using AUTOCLIK and AUTODRIV
AUTOCLIK is a simple Automation server sample application that you can use as a base from which to learn more about Remote Automation. AUTODRIV is a simple Automation client application that drives AUTOCLIK. You can use them to demonstrate Remote Automation.  
  
#### To install AUTOCLIK.EXE on two machines and drive it using Remote Automation  
  
1.  Install the [AUTOCLIK](../vs140/Visual-C---Samples.md) sample application onto your development machine.  
  
2.  Build AUTOCLIK.EXE.  
  
3.  Run AUTOCLIK.EXE in standalone fashion and then shut it down. This will register it as an Automation server.  
  
4.  Copy AUTOCLIK.EXE to a remote machine, run it there, and then shut it down.  
  
5.  Run AUTODRIV.EXE on the local machine and verify that running it starts AUTOCLIK.EXE. To find out more about AUTODRIV.EXE, see [AUTOCLIK](../vs140/Visual-C---Samples.md).  
  
6.  On the remote machine, start AUTMGR32.EXE (Automation Manager).  
  
7.  On the remote machine, start RACMGR32.EXE (Remote Automation Connection Manager).  
  
8.  In the Remote Automation Connection Manager, select AutoClik.Document from the **OLE Classes** list.  
  
9. Choose a system security policy from the **Client Access** tab to grant client access to AutoClik.Document.  
  
10. On the local machine, start RACMGR32.EXE and select AutoClik.Document from the **OLE Classes** list.  
  
11. From the **Server Connection** tab, choose both the network address of the remote machine and the appropriate network protocol.  
  
12. With AutoClik.Document still selected in the **OLE Classes** list box, choose the **Remote** command from the `Register` menu.  
  
13. On the local machine, run AUTODRIV.EXE or the equivalent AUTOCLIK.MAK Visual Basic project if you want to have a Visual Basic, rather than an MFC, client.  
  
 On the remote machine, you should now be able to see AUTOCLIK executing commands initiated from the local client.  
  
## See Also  
 [Remote Automation](../vs140/Remote-Automation.md)