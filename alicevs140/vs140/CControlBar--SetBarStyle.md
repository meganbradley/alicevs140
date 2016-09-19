---
title: "CControlBar::SetBarStyle"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 1c56ed8c-4d5a-4351-811b-fb82014e68c8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::SetBarStyle
Call this function to set the desired **CBRS_** styles for the control bar.  
  
## Syntax  
  
```  
  
      void SetBarStyle(  
   DWORD dwStyle   
);  
```  
  
#### Parameters  
 `dwStyle`  
 The desired styles for the control bar. Can be one or more of the following:  
  
-   `CBRS_ALIGN_TOP` Allows the control bar to be docked to the top of the client area of a frame window.  
  
-   `CBRS_ALIGN_BOTTOM` Allows the control bar to be docked to the bottom of the client area of a frame window.  
  
-   `CBRS_ALIGN_LEFT` Allows the control bar to be docked to the left side of the client area of a frame window.  
  
-   `CBRS_ALIGN_RIGHT` Allows the control bar to be docked to the right side of the client area of a frame window.  
  
-   `CBRS_ALIGN_ANY` Allows the control bar to be docked to any side of the client area of a frame window.  
  
-   `CBRS_BORDER_TOP` Causes a border to be drawn on the top edge of the control bar when it would be visible.  
  
-   `CBRS_BORDER_BOTTOM` Causes a border to be drawn on the bottom edge of the control bar when it would be visible.  
  
-   `CBRS_BORDER_LEFT` Causes a border to be drawn on the left edge of the control bar when it would be visible.  
  
-   `CBRS_BORDER_RIGHT` Causes a border to be drawn on the right edge of the control bar when it would be visible.  
  
-   `CBRS_FLOAT_MULTI` Allows multiple control bars to be floated in a single mini-frame window.  
  
-   `CBRS_TOOLTIPS` Causes tool tips to be displayed for the control bar.  
  
-   `CBRS_FLYBY` Causes message text to be updated at the same time as tool tips.  
  
-   **CBRS_GRIPPER** Causes a gripper, similar to that used on bands in a **CReBar** object, to be drawn for any `CControlBar`-derived class.  
  
## Remarks  
 Does not affect the **WS_** (window style) settings.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::GetBarStyle](../vs140/CControlBar--GetBarStyle.md)