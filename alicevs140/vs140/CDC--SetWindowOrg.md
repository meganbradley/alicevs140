---
title: "CDC::SetWindowOrg"
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
ms.assetid: ef4e9dc9-03be-4cbe-abe9-27b1a0a5652d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetWindowOrg
Sets the window origin of the device context.  
  
## Syntax  
  
```  
  
      CPoint SetWindowOrg(  
   int x,  
   int y   
);  
CPoint SetWindowOrg(  
   POINT point   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the new origin of the window.  
  
 *y*  
 Specifies the logical y-coordinate of the new origin of the window.  
  
 `point`  
 Specifies the logical coordinates of the new origin of the window. You can pass either a **POINT** structure or a `CPoint` object for this parameter.  
  
## Return Value  
 The previous origin of the window as a `CPoint` object.  
  
## Remarks  
 The window, along with the device-context viewport, defines how GDI maps points in the logical coordinate system to points in the device coordinate system.  
  
 The window origin marks the point in the logical coordinate system from which GDI maps the viewport origin, a point in the device coordinate system specified by the **SetWindowOrg** function. GDI maps all other points by following the same process required to map the window origin to the viewport origin. For example, all points in a circle around the point at the window origin will be in a circle around the point at the viewport origin. Similarly, all points in a line that passes through the window origin will be in a line that passes through the viewport origin.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [CDC::GetWindowOrg](../vs140/CDC--GetWindowOrg.md)