---
title: "Debugger Cannot Display Source Code or Disassembly"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 112d3ea3-fdd2-4bce-92b4-167a76258934
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugger Cannot Display Source Code or Disassembly
This error reads:  
  
 The debugger cannot display source code or disassembly for the current location where execution has stopped.  
  
 This error message can occur for a number of reasons:  
  
-   You may have hit a breakpoint in a location for which there is no source code, while debugging a language that doesn't support disassembly. Open the **Breakpoints** window, locate the breakpoint, and delete it.  
  
-   If you are debugging script, you may have hit a breakpoint while there were no threads in your program. Choose **Step** or **Continue** from the **Debug** menu to resume debugging.  
  
-   Security considerations may have prevented the debugger from reading stack, thread, register, and other context information from the program you are debugging. This is most likely to happen if you are debugging a Web application and don't have the right permission to access the virtual directory. Set security for the virtual directory to Anonymous and try again.  
  
## See Also  
 [Debugger Basics](../vs140/Debugger-Basics.md)   
 [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md)   
 [Viewing Data in the Debugger](../vs140/Viewing-Data-in-the-Debugger.md)