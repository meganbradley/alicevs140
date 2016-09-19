---
title: "Window Destruction Sequence"
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
ms.assetid: 2d819196-6240-415f-a308-db43745e616c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Window Destruction Sequence
In the MFC framework, when the user closes the frame window, the window's default [OnClose](../vs140/CWnd--OnClose.md) handler calls [DestroyWindow](../vs140/CWnd--DestroyWindow.md). The last member function called when the Windows window is destroyed is [OnNcDestroy](../vs140/CWnd--OnNcDestroy.md), which does some cleanup, calls the [Default](../vs140/CWnd--Default.md) member function to perform Windows cleanup, and lastly calls the virtual member function [PostNcDestroy](../vs140/CWnd--PostNcDestroy.md). The [CFrameWnd](../vs140/CFrameWnd-Class.md) implementation of `PostNcDestroy` deletes the C++ window object.  
  
## What do you want to know more about?  
  
-   [Allocating and deallocating window memory](../vs140/Allocating-and-Deallocating-Window-Memory.md)  
  
-   [Detaching a CWnd from its HWND](../vs140/Detaching-a-CWnd-from-Its-HWND.md)  
  
## See Also  
 [Destroying Window Objects](../vs140/Destroying-Window-Objects.md)