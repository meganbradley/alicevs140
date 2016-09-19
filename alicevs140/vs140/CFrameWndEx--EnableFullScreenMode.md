---
title: "CFrameWndEx::EnableFullScreenMode"
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
ms.topic: reference
ms.assetid: 2b24a30e-acb4-48df-872d-6f836ec790a6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::EnableFullScreenMode
Enables the full-screen mode for the frame window.  
  
## Syntax  
  
```  
void EnableFullScreenMode(  
   UINT uiFullScreenCmd   
);  
```  
  
#### Parameters  
 [in] `uiFullScreenCmd`  
 The ID of a command that enables and disables the full screen mode.  
  
## Remarks  
 In the full-screen mode, all docking control bars, toolbars and menu are hidden and the active view is resized to occupy the full-screen.  
  
 When you enable the full-screen mode, you must specify an ID of the command that enables or disables the full-screen mode. You can call `EnableFullScreenMode` from the main frame's `OnCreate` function. When a frame window is being switched to a full-screen mode, the framework creates a floating toolbar with one button that has the specified command ID.  
  
 If you want to keep the main menu on the screen, call [CFrameWndEx::EnableFullScreenMainMenu](../vs140/CFrameWndEx--EnableFullScreenMainMenu.md).  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)