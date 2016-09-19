---
title: "Tips for Debugging Threads in Native Code"
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
ms.assetid: 0374c8c6-57a3-4cfe-8047-2effef5ff5dc
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tips for Debugging Threads in Native Code
Here are some tips you can use when debugging threads in native code:  
  
-   You can view the contents of the Thread Information Block by typing `@TIB` in the **Watch** window or **QuickWatch** dialog box.  
  
-   You can view the last error code for the current thread by entering `@Err` in the **Watch** window or **QuickWatch** dialog box.  
  
-   C Run-Time Libraries (CRT) functions can be useful for debugging a multithreaded application. For more information, see [_malloc_dbg](../vs140/_malloc_dbg.md).  
  
## See Also  
 [Debugging Multithreaded Applications](../vs140/Debug-Multithreaded-Applications-in-Visual-Studio.md)   
 [Debugging Native Code](../vs140/Debugging-Native-Code.md)