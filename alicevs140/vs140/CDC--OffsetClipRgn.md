---
title: "CDC::OffsetClipRgn"
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
ms.assetid: d39e4bca-89d2-440b-bfbb-15619f7bd2f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::OffsetClipRgn
Moves the clipping region of the device context by the specified offsets.  
  
## Syntax  
  
```  
  
      int OffsetClipRgn(  
   int x,  
   int y   
);  
int OffsetClipRgn(  
   SIZE size   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the number of logical units to move left or right.  
  
 *y*  
 Specifies the number of logical units to move up or down.  
  
 `size`  
 Specifies the amount to offset.  
  
## Return Value  
 The new region's type. It can be any one of the following values:  
  
-   **COMPLEXREGION** Clipping region has overlapping borders.  
  
-   **ERROR** Device context is not valid.  
  
-   **NULLREGION** Clipping region is empty.  
  
-   **SIMPLEREGION** Clipping region has no overlapping borders.  
  
## Remarks  
 The function moves the region *x* units along the x-axis and *y* units along the y-axis.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SelectClipRgn](../vs140/CDC--SelectClipRgn.md)   
 [OffsetClipRgn](http://msdn.microsoft.com/library/windows/desktop/dd162745)