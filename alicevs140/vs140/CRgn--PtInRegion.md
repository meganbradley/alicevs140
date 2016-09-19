---
title: "CRgn::PtInRegion"
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
ms.assetid: 7de1fc52-8adf-432a-8861-3944e058dd51
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::PtInRegion
Checks whether the point given by *x* and *y* is in the region stored in the `CRgn` object.  
  
## Syntax  
  
```  
  
      BOOL PtInRegion(  
   int x,  
   int y   
) const;  
BOOL PtInRegion(  
   POINT point   
) const;  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the point to test.  
  
 *y*  
 Specifies the logical y-coordinate of the point to test.  
  
 `point`  
 The x- and y-coordinates of `point` specify the x- and y-coordinates of the point to test the value of. The `point` parameter can either be a **POINT** structure or a `CPoint` object.  
  
## Return Value  
 Nonzero if the point is in the region; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PtInRegion](http://msdn.microsoft.com/library/windows/desktop/dd162883)