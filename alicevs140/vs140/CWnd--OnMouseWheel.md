---
title: "CWnd::OnMouseWheel"
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
ms.assetid: 6cce8175-77a9-49cd-a150-5d68de2c28b0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnMouseWheel
The framework calls this member function as a user rotates the mouse wheel and encounters the wheel's next notch.  
  
## Syntax  
  
```  
  
      afx_msg BOOL OnMouseWheel(  
   UINT nFlags,  
   short zDelta,  
   CPoint pt   
);  
```  
  
#### Parameters  
 `nFlags`  
 Indicates whether various virtual keys are down. This parameter can be any combination of the following values:  
  
-   **MK_CONTROL** Set if the CTRL key is down.  
  
-   **MK_LBUTTON** Set if the left mouse button is down.  
  
-   **MK_MBUTTON** Set if the middle mouse button is down.  
  
-   **MK_RBUTTON** Set if the right mouse button is down.  
  
-   **MK_SHIFT** Set if the SHIFT key is down.  
  
 `zDelta`  
 Indicates distance rotated. The `zDelta` value is expressed in multiples or divisions of **WHEEL_DELTA**, which is 120. A value less than zero indicates rotating back (toward the user) while a value greater than zero indicates rotating forward (away from the user). The user can reverse this response by changing the Wheel setting in the mouse software. See the Remarks for more information about this parameter.  
  
 `pt`  
 Specifies the x- and y-coordinate of the cursor. These coordinates are always relative to the upper-left corner of the screen.  
  
## Return Value  
 Nonzero if mouse wheel scrolling is enabled; otherwise 0.  
  
## Remarks  
 Unless overridden, `OnMouseWheel` calls the default of [WM_MOUSEWHEEL](http://msdn.microsoft.com/library/windows/desktop/ms645617). Windows automatically routes the message to the control or child window that has the focus. The Win32 function [DefWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633572) propagates the message up the parent chain to the window that processes it.  
  
 The `zDelta` parameter is a multiple of **WHEEL_DELTA**, which is set at 120. This value is the threshold for an action to be taken, and one such action (for example, scrolling forward one notch) should occur for each delta.  
  
 **WHEEL_DELTA** was set to 120 to allow for finer-resolution wheels, such as a freely-rotating wheel with no notches. A finer-resolution wheel sends more messages per rotation, but each message has a smaller delta value. To use such a wheel, either add the incoming `zDelta` values until **WHEEL_DELTA** is reached (so that you get the same response for a given delta-rotation), or scroll partial lines in response to the more frequent messages. You can also choose a scroll granularity and accumulate deltas until **WHEEL_DELTA** is reached.  
  
 Override this member function to provide your own mouse-wheel scrolling behavior.  
  
> [!NOTE]
>  `OnMouseWheel` handles messages for Windows NT 4.0 and later versions. For Windows 95/98 or Windows NT 3.51 message handling, use [OnRegisteredMouseWheel](../vs140/CWnd--OnRegisteredMouseWheel.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnMouseMove](../vs140/CWnd--OnMouseMove.md)