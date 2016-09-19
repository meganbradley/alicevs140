---
title: "CDC::FloodFill"
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
ms.assetid: 2a66a229-d1e7-44b1-9c98-420c9bb6bcb9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::FloodFill
Fills an area of the display surface with the current brush.  
  
## Syntax  
  
```  
  
      BOOL FloodFill(  
   int x,  
   int y,  
   COLORREF crColor   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the point where filling begins.  
  
 *y*  
 Specifies the logical y-coordinate of the point where filling begins.  
  
 `crColor`  
 Specifies the color of the boundary.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0 is returned if the filling could not be completed, the given point has the boundary color specified by `crColor`, or the point is outside the clipping region.  
  
## Remarks  
 The area is assumed to be bounded as specified by `crColor`. The `FloodFill` function begins at the point specified by *x* and *y* and continues in all directions to the color boundary.  
  
 Only memory-device contexts and devices that support raster-display technology support the `FloodFill` member function. For information about **RC_BITBLT** capability, see the `GetDeviceCaps` member function.  
  
 The `ExtFloodFill` function provides similar capability but greater flexibility.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::ExtFloodFill](../vs140/CDC--ExtFloodFill.md)   
 [CDC::GetDeviceCaps](../vs140/CDC--GetDeviceCaps.md)   
 [FloodFill](http://msdn.microsoft.com/library/windows/desktop/dd162726)