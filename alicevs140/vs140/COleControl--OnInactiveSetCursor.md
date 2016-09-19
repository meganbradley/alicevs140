---
title: "COleControl::OnInactiveSetCursor"
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
ms.assetid: 430ee37d-614b-468a-8335-e8fe683e66a6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnInactiveSetCursor
Called by the container for the inactive object under the mouse pointer on receipt of a `WM_SETCURSOR` message.  
  
## Syntax  
  
```  
  
      virtual BOOL OnInactiveSetCursor(  
   LPCRECT lprcBounds,  
   long x,  
   long y,  
   DWORD dwMouseMsg,  
   BOOL bSetAlways   
);  
```  
  
#### Parameters  
 `lprcBounds`  
 The object bounding rectangle, in client coordinates of the containing window. Tells the object its exact position and size on the screen when the `WM_SETCURSOR` message was received.  
  
 *x*  
 The x coordinate of the mouse location in client coordinates of the containing window.  
  
 *y*  
 The y coordinate of the mouse location in client coordinates of the containing window.  
  
 *dwMouseMsg*  
 The identifier of the mouse message for which a `WM_SETCURSOR` occurred.  
  
 *bSetAlways*  
 Specifies whether or not the object must set the cursor. If **TRUE**, the object must set the cursor; if **FALSE**, the cursor is not obligated to set the cursor, and should return **S_FALSE** in that case.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Note that window client coordinates (pixels) are used to pass the mouse cursor position. This is made possible by also passing the bounding rectangle of the object in the same coordinate system.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetActivationPolicy](../vs140/COleControl--GetActivationPolicy.md)   
 [COleControl::OnInactiveMouseMove](../vs140/COleControl--OnInactiveMouseMove.md)