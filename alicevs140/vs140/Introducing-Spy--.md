---
title: "Introducing Spy++"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 733b514b-63a9-402d-89aa-4f0416766655
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Introducing Spy++
Spy++ lets you perform the following tasks:  
  
-   Display a graphical tree of relationships among system objects. These include [processes](../vs140/Processes-View.md), [threads](../vs140/Threads-View.md), and [windows](../vs140/Windows-View.md).  
  
-   Search for specified [windows](../vs140/How-to--Search-for-a-Window-in-Windows-View.md), [threads](../vs140/How-to--Search-for-a-Thread-in-Threads-View.md), [processes](../vs140/How-to--Search-for-a-Process-in-Processes-View.md), or [messages](../vs140/How-to--Search-for-a-Message-in-Messages-View.md).  
  
-   View the properties of selected [windows](../vs140/How-to--Display-Window-Properties.md), [threads](../vs140/How-to--Display-Thread-Properties.md), [processes](../vs140/How-to--Display-Process-Properties.md), or [messages](../vs140/How-to--Display-Message-Properties.md).  
  
-   Select a window, thread, process, or message directly in the view.  
  
-   Use the [Finder Tool](../vs140/How-to--Use-the-Finder-Tool.md) to select a window by mouse pointer positioning.  
  
-   Set [message options](_asug_choosing_message_options) by using complex message log selection parameters.  
  
 Spy++ has a toolbar and hyperlinks to help you work faster. It also provides a **Refresh** command to update the active view, a **Window Finder Tool** to make spying easier, and a **Font** dialog box to customize view windows. Additionally, Spy++ lets you save and restore user preferences.  
  
 In various Spy++ windows, you can right-click to display a shortcut menu of frequently used commands. Which commands are displayed depends on where the pointer is. For example, if you right-click an entry in the Window view and the selected window is visible, then clicking **Highlight** on the shortcut menu causes the border of the selected window to flash so that it can be located more easily.  
  
> [!NOTE]
>  There are two other utilities that resemble Spy++: PView, which shows details about processes and threads, and DDESPY.EXE, which lets you monitor Dynamic Data Exchange (DDE) messages.  
  
## 64-Bit Operating Systems  
 There are two versions of Spy++. The first version, named Spy++ (spyxx.exe), is designed to display messages sent to a window that is running in a 32-bit process. For example, Visual Studio runs in a 32-bit process. Therefore, you can use Spy++ to display messages sent to **Solution Explorer**. Because the default configuration for most builds in Visual Studio is to run in a 32-bit process, this first version of Spy++ is the one that is available on the **Tools** menu in Visual Studio.  
  
 The second version, named Spy++ (64-bit) (spyxx_amd64.exe), is designed to display messages sent to a window that is running in a 64-bit process. For example, on a 64-bit operating system, Notepad runs in a 64-bit process. Therefore, you can use Spy++ (64-bit) to display messages sent to Notepad. Spy++ (64-bit) is typically located in  
  
 ..\\*Visual Studio installation folder*\Common7\Tools\spyxx_amd64.exe.  
  
 You can run either version of Spy++ directly from the command line.  
  
> [!NOTE]
>  Although the Spy++ (64-bit) file name contains "amd", it runs on any x64 Windows operating system.  
  
## See Also  
 [Using Spy++](../vs140/Using-Spy--.md)   
 [Spy++ Views](../vs140/Spy---Views.md)   
 [Spy++ Reference](../vs140/Spy---Reference.md)