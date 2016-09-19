---
title: "CDC::PtVisible"
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
ms.assetid: 04775cc7-0002-41e5-bba8-e1e075648d01
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PtVisible
Determines whether the given point is within the clipping region of the device context.  
  
## Syntax  
  
```  
  
      virtual BOOL PtVisible(  
   int x,  
   int y   
) const;  
BOOL PtVisible(  
   POINT point   
) const;  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the point.  
  
 *y*  
 Specifies the logical y-coordinate of the point.  
  
 `point`  
 Specifies the point to check in logical coordinates. You can pass either a **POINT** structure or a `CPoint` object for this parameter.  
  
## Return Value  
 Nonzero if the specified point is within the clipping region; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::RectVisible](../vs140/CDC--RectVisible.md)   
 [CDC::SelectClipRgn](../vs140/CDC--SelectClipRgn.md)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [PtVisible](http://msdn.microsoft.com/library/windows/desktop/dd162890)   
 [POINT Structure](../vs140/POINT-Structure.md)