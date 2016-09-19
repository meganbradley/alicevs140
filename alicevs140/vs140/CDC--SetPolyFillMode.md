---
title: "CDC::SetPolyFillMode"
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
ms.assetid: 9519f767-8e99-400c-83ee-1ab28518c3a0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetPolyFillMode
Sets the polygon-filling mode.  
  
## Syntax  
  
```  
  
      int SetPolyFillMode(  
   int nPolyFillMode   
);  
```  
  
#### Parameters  
 `nPolyFillMode`  
 Specifies the new filling mode. This value may be either **ALTERNATE** or **WINDING**. The default mode set in Windows is **ALTERNATE**.  
  
## Return Value  
 The previous filling mode, if successful; otherwise 0.  
  
## Remarks  
 When the polygon-filling mode is **ALTERNATE**, the system fills the area between odd-numbered and even-numbered polygon sides on each scan line. That is, the system fills the area between the first and second side, between the third and fourth side, and so on. This mode is the default.  
  
 When the polygon-filling mode is **WINDING**, the system uses the direction in which a figure was drawn to determine whether to fill an area. Each line segment in a polygon is drawn in either a clockwise or a counterclockwise direction. Whenever an imaginary line drawn from an enclosed area to the outside of a figure passes through a clockwise line segment, a count is incremented. When the line passes through a counterclockwise line segment, the count is decremented. The area is filled if the count is nonzero when the line reaches the outside of the figure.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetPolyFillMode](../vs140/CDC--GetPolyFillMode.md)   
 [CDC::PolyPolygon](../vs140/CDC--PolyPolygon.md)   
 [SetPolyFillMode](http://msdn.microsoft.com/library/windows/desktop/dd145080)