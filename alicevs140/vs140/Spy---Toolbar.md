---
title: "Spy++ Toolbar"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 949c18fb-bb25-42ed-9130-c4a47869f24d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Spy++ Toolbar
The toolbar appears under the menu bar in Spy++. To display or hide the toolbar, on the **View** menu, click **Toolbar**.  
  
 The following controls are available on the toolbar.  
  
## UIElement List  
  
|Button|Effect|  
|------------|------------|  
|![Spy&#43;&#43; Windows Button](../vs140/media/Icon_Spy--_Windows.gif "Icon_Spy++_Windows")|Displays a tree view of the windows and controls in the system. For more information, see [Windows View](../vs140/Windows-View.md).|  
|![Spy&#43;&#43; Processes Button](../vs140/media/Icon_Spy--_Processes.gif "Icon_Spy++_Processes")|Displays a tree view of the processes in the system. For more information, see [Processes View](../vs140/Processes-View.md).|  
|![Spy&#43;&#43; Threads Button](../vs140/media/Icon_Spy--_Threads.gif "Icon_Spy++_Threads")|Displays a tree view of the threads in the system. For more information, see [Threads View](../vs140/Threads-View.md).|  
|![Spy&#43;&#43; Messages Button](../vs140/media/Icon_Spy--_Messages.gif "Icon_Spy++_Messages")|Creates a window to display window messages and opens the **Message Options** dialog box so that you can select the window whose messages will be displayed and also select other options. For more information, see [Messages View](../vs140/Messages-View.md).|  
|![Spy&#43;&#43; Start Log Button](../vs140/media/Icon_Spy--_StartLog.gif "Icon_Spy++_StartLog")|Starts message logging and displays the message stream. This control is available only when a **Messages** window is the active window. For more information, see [How to: Start and Stop the Message Log Display](../vs140/How-to--Start-and-Stop-the-Message-Log-Display.md).|  
|![Spy&#43;&#43; Stop Log Button](../vs140/media/Icon_Spy--_StopLog.gif "Icon_Spy++_StopLog")|Stops message logging and the display of the message stream. This control is available only when a **Messages** window is the active window. For more information, see [How to: Start and Stop the Message Log Display](../vs140/How-to--Start-and-Stop-the-Message-Log-Display.md).|  
|![Spy&#43;&#43; Log Options Button](../vs140/media/Icon_Spy--_LogOptions.gif "Icon_Spy++_LogOptions")|Displays the [Message Options](../vs140/Message-Options-Dialog-Box.md) dialog box. Use this dialog box to select windows and message types for viewing. This control is available only when a **Messages** window is the active window.|  
|![Spy&#43;&#43; Clear Log Button](../vs140/media/Spy--_ClearLog.gif "Spy++_ClearLog")|Clears the contents of the active **Messages** window. This control is available only when a **Messages** window is the active window.|  
|![Spy&#43;&#43; Find Window Button](../vs140/media/Icon_Spy--_FindWindow.gif "Icon_Spy++_FindWindow")|Opens the [Find Window](../vs140/Find-Window-Dialog-Box.md) dialog box, which lets you set window search criteria and display properties or messages. For more information, see [How to: Use the Finder Tool](../vs140/How-to--Use-the-Finder-Tool.md).|  
|![Spy&#43;&#43; Find First Window Button](../vs140/media/Icon_Spy--_Window.gif "Icon_Spy++_Window")|Searches the current view for a matching window, process, thread, or message.|  
|![Spy&#43;&#43; Find Next Window Button](../vs140/media/Icon_Spy--_NextWindow.gif "Icon_Spy++_NextWindow")|Searches the current view for the next matching window, process, thread, or message. This control (and the related menu command) is available only when there is a valid search result that is not unique. For example, when you use a window handle as the search criterion in the window tree, it produces unique results because there is only one window in the window tree that has that handle; in this instance, **Find Next** is not available.|  
|![Spy&#43;&#43; Find Previous Window Button](../vs140/media/Icon_Spy--_PrevWindow.gif "Icon_Spy++_PrevWindow")|Searches the current view for the previous matching window, process, thread, or message. This control (and the related menu command) is available only when there is a valid search result that is not unique. For example, when you use a window handle as the search criterion in the window tree, it produces unique results because there is only one window in the window tree that has that handle; in this instance, **Find Previous** is not available.|  
|![Spy&#43;&#43; Property Explorer Button](../vs140/media/Icon_Spy--_PropExp.gif "Icon_Spy++_PropExp")|Displays the properties of the window that is selected in the Windows view.|  
|![Spy&#43;&#43; Refresh Button](../vs140/media/Icon_Spy--_Refresh.gif "Icon_Spy++_Refresh")|Refreshes the system views.|  
  
## See Also  
 [Using Spy++](../vs140/Using-Spy--.md)   
 [Spy++ Views](../vs140/Spy---Views.md)   
 [Spy++ Reference](../vs140/Spy---Reference.md)