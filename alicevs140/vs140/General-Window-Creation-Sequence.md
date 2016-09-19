---
title: "General Window Creation Sequence"
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
ms.assetid: 9cd8c7ea-5e24-429e-b6d9-d7b6041d8ba6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# General Window Creation Sequence
When you create a window of your own, such as a child window, the framework uses much the same process as that described in [Document/View Creation](../vs140/Document-View-Creation.md).  
  
 All the window classes provided by MFC employ [two-stage construction](../vs140/One-Stage-and-Two-Stage-Construction-of-Objects.md). That is, during an invocation of the C++ **new** operator, the constructor allocates and initializes a C++ object but does not create a corresponding Windows window. That is done afterward by calling the [Create](../vs140/CWnd--Create.md) member function of the window object.  
  
 The **Create** member function makes the Windows window and stores its `HWND` in the C++ object's public data member [m_hWnd](../vs140/CWnd--m_hWnd.md). **Create** gives complete flexibility over the creation parameters. Before calling **Create**, you may want to register a window class with the global function [AfxRegisterWndClass](../vs140/AfxRegisterWndClass.md) in order to set the icon and class styles for the frame.  
  
 For frame windows, you can use the [LoadFrame](../vs140/CFrameWnd--LoadFrame.md) member function instead of **Create**. `LoadFrame` makes the Windows window using fewer parameters. It gets many default values from resources, including the frame's caption, icon, accelerator table, and menu.  
  
> [!NOTE]
>  Your icon, accelerator table, and menu resources must have a common resource ID, such as **IDR_MAINFRAME**, for them to be loaded by LoadFrame.  
  
## What do you want to know more about?  
  
-   [Window objects](../vs140/Window-Objects.md)  
  
-   [Registering window "classes"](../vs140/Registering-Window-Classes.md)  
  
-   [Destroying window objects](../vs140/Destroying-Window-Objects.md)  
  
-   [Creating document frame windows](../vs140/Creating-Document-Frame-Windows.md)  
  
## See Also  
 [Creating Windows](../vs140/Creating-Windows.md)