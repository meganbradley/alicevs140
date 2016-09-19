---
title: "How to: Switch to Another Thread While Debugging"
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
ms.assetid: 5cd76c52-76fa-4fcc-b37e-e9f0ecac0e9e
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Switch to Another Thread While Debugging
When you debug a multithreaded application, you can use any one of several methods to switch the context from the thread that you have been working with to another thread.  
  
### To switch to any thread that appears in the Threads window  
  
-   Double-click the thread.  
  
### To switch to a thread in a source window  
  
-   In the left gutter, right-click a thread indicator, point to **Switch to**, and then click the name of that thread to which you want to switch. The shortcut menu shows only the threads at that specific location.  
  
     If no indicators appear, right-click in the **Threads** window and verify that **Show Threads in Source** is selected.  
  
### To switch to a thread in the Debug Location toolbar  
  
1.  On the **Debug Location** toolbar, click the **Thread** box.  
  
2.  In the list, click the thread to which you want to switch.  
  
## See Also  
 [Debugging Multithreaded Applications](../vs140/Debug-Multithreaded-Applications-in-Visual-Studio.md)