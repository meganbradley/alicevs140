---
title: "How to: Use the Parallel Watch Window"
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
ms.assetid: 28004d9b-420c-48f7-b80e-ab1519802558
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use the Parallel Watch Window
In the Parallel Watch window, you can simultaneously display the values that one expression holds on multiple threads. Each row represents a thread that is running in an application, but a thread might be represented in multiple rows. More specifically, each row represents a function call whose function signature matches the function on the current stack frame. You can sort, reorder, remove, and group the items that are in the columns. You can flag, unflag, freeze (suspend), and thaw (resume) threads. The following columns are displayed in the **Parallel Watch** window:  
  
-   The flag column, in which you can mark a thread that you want to pay special attention to.  
  
-   The frame column, in which an arrow indicates the selected frame.  
  
-   A configurable column that can display the machine, process, tile, task, and thread.  
  
    > [!TIP]
    >  You must open the **Parallel Task** window to display the task information in the **Parallel Watch** window.  
  
-   The **<Add Watch\>** column, in which you can enter expressions to watch.  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
### To display the Parallel Watch window  
  
1.  Set a breakpoint in the code.  
  
2.  On the menu bar, choose **Debug**, **Start Debugging**. Wait for the application to reach the breakpoint.  
  
3.  On the menu bar, choose **Debug**, **Windows**, **Parallel Watch**, and then choose a watch window. You can open as many as four windows.  
  
### To add a watch expression  
  
-   Select **<Add Watch\>** and then specify a watch expression.  
  
### To flag or unflag a thread  
  
-   Select the flag column for the row, or open the shortcut menu for the thread and choose **Flag** or **Unflag**.  
  
### To display only flagged threads  
  
-   Choose the Show Flagged Only button in the upper-left corner of the **Parallel Watch** window.  
  
### To switch frames  
  
-   Double-click the frame column. (Keyboard: Select the row and press Enter.)  
  
### To sort a column  
  
-   Select the column heading.  
  
### To group threads  
  
-   Open the shortcut menu for the Parallel Watch window, choose **Group By**, and then choose the appropriate submenu item.  
  
### To freeze or thaw threads  
  
-   Open the shortcut menu for the row and choose **Freeze** or **Thaw**.  
  
### To export the data in the Parallel Watch window  
  
-   Choose the **Open in Excel** button and then choose **Open in Excel** or **Export to CSV**.  
  
### To filter by a Boolean expression  
  
-   Enter a Boolean expression in the **Filter by Boolean Expression** box. The debugger evaluates the expression for each thread context. Only rows where the value is `true` are displayed.  
  
## See Also  
 [Debugging Multithreaded Applications](../vs140/Debug-Multithreaded-Applications-in-Visual-Studio.md)   
 [How to: Use the GPU Threads Window](../vs140/How-to--Use-the-GPU-Threads-Window.md)   
 [Walkthrough: Debugging a C++ AMP Application](../vs140/Walkthrough--Debugging-a-C---AMP-Application.md)