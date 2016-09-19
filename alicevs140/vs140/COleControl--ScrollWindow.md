---
title: "COleControl::ScrollWindow"
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
ms.assetid: 6544ecfc-88eb-4087-9ac5-04adf8fe50aa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ScrollWindow
Allows a windowless OLE object to scroll an area within its in-place active image on the screen.  
  
## Syntax  
  
```  
  
      void ScrollWindow(  
   int xAmount,  
   int yAmount,  
   LPCRECT lpRect = NULL,  
   LPCRECT lpClipRect = NULL   
);  
```  
  
#### Parameters  
 `xAmount`  
 Specifies the amount, in device units, of horizontal scrolling. This parameter must be a negative value to scroll to the left.  
  
 `yAmount`  
 Specifies the amount, in device units, of vertical scrolling. This parameter must be a negative value to scroll upward.  
  
 `lpRect`  
 Points to a [CRect](../vs140/CRect-Class.md) object or [RECT](../vs140/RECT-Structure.md) structure that specifies the portion of the OLE object's client area to scroll, in client coordinates of the containing window. If `lpRect` is **NULL**, the entire OLE object's client area is scrolled.  
  
 `lpClipRect`  
 Points to a `CRect` object or `RECT` structure that specifies the rectangle to clip to. Only pixels inside the rectangle are scrolled. Bits outside the rectangle are not affected even if they are in the `lpRect` rectangle. If `lpClipRect` is **NULL**, no clipping is performed on the scroll rectangle.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)