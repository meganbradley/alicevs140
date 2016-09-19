---
title: "CControlBar::EnableDocking"
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
ms.assetid: 03129947-b08f-418f-a09a-e637cf1e7c64
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::EnableDocking
Call this function to enable a control bar to be docked.  
  
## Syntax  
  
```  
  
      void EnableDocking(  
   DWORD dwDockStyle   
);  
```  
  
#### Parameters  
 `dwDockStyle`  
 Specifies whether the control bar supports docking and the sides of its parent window to which the control bar can be docked, if supported. Can be one or more of the following:  
  
-   `CBRS_ALIGN_TOP` Allows docking at the top of the client area.  
  
-   `CBRS_ALIGN_BOTTOM` Allows docking at the bottom of the client area.  
  
-   `CBRS_ALIGN_LEFT` Allows docking on the left side of the client area.  
  
-   `CBRS_ALIGN_RIGHT` Allows docking on the right side of the client area.  
  
-   `CBRS_ALIGN_ANY` Allows docking on any side of the client area.  
  
-   `CBRS_FLOAT_MULTI` Allows multiple control bars to be floated in a single mini-frame window.  
  
 If 0 (that is, indicating no flags), the control bar will not dock.  
  
## Remarks  
 The sides specified must match one of the sides enabled for docking in the destination frame window, or the control bar cannot be docked to that frame window.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::EnableDocking](../vs140/CFrameWnd--EnableDocking.md)   
 [CFrameWnd::DockControlBar](../vs140/CFrameWnd--DockControlBar.md)   
 [CFrameWnd::FloatControlBar](../vs140/CFrameWnd--FloatControlBar.md)   
 [CControlBar::SetBarStyle](../vs140/CControlBar--SetBarStyle.md)