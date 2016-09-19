---
title: "CDC::SetPixelV"
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
ms.assetid: 9dbd4d4f-151d-463f-b57d-acd69fd37c79
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetPixelV
Sets the pixel at the specified coordinates to the closest approximation of the specified color.  
  
## Syntax  
  
```  
  
      BOOL SetPixelV(  
   int x,  
   int y,  
   COLORREF crColor  
);  
BOOL SetPixelV(  
   POINT point,  
   COLORREF crColor   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the x-coordinate, in logical units, of the point to be set.  
  
 *y*  
 Specifies the y-coordinate, in logical units, of the point to be set.  
  
 `crColor`  
 Specifies the color to be used to paint the point.  
  
 `point`  
 Specifies the logical x- and y-coordinates of the point to be set. You can pass either a [POINT](../vs140/POINT-Structure.md) data structure or a [CPoint](../vs140/CPoint-Class.md) object for this parameter.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The point must be in both the clipping region and the visible part of the device surface. Not all devices support the member function. For more information, see the **RC_BITBLT** capability in the `CDC::GetDeviceCaps` member function. `SetPixelV` is faster than `SetPixel` because it does not need to return the color value of the point actually painted.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetDeviceCaps](../vs140/CDC--GetDeviceCaps.md)   
 [CDC::SetPixel](../vs140/CDC--SetPixel.md)   
 [SetPixelV](http://msdn.microsoft.com/library/windows/desktop/dd145079)