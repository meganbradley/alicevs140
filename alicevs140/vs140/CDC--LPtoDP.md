---
title: "CDC::LPtoDP"
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
ms.assetid: 70d1438d-57f9-4390-9486-f6ceb58da1c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::LPtoDP
Converts logical units into device units.  
  
## Syntax  
  
```  
  
      void LPtoDP(  
   LPPOINT lpPoints,  
   int nCount = 1   
) const;  
void LPtoDP(  
   LPRECT lpRect   
) const;  
void LPtoDP(  
   LPSIZE lpSize   
) const;  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of points. Each point in the array is a [POINT](../vs140/POINT-Structure.md) structure or a [CPoint](../vs140/CPoint-Class.md) object.  
  
 `nCount`  
 The number of points in the array.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or a [CRect](../vs140/CRect-Class.md) object. This parameter is used for the common case of mapping a rectangle from logical to device units.  
  
 `lpSize`  
 Points to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or a [CSize](../vs140/CSize-Class.md) object.  
  
## Remarks  
 The function maps the coordinates of each point, or dimensions of a size, from GDI's logical coordinate system into a device coordinate system. The conversion depends on the current mapping mode and the settings of the origins and extents of the device's window and viewport.  
  
 The x- and y-coordinates of points are 2-byte signed integers in the range –32,768 through 32,767. In cases where the mapping mode would result in values larger than these limits, the system sets the values to –32,768 and 32,767, respectively.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::DPtoLP](../vs140/CDC--DPtoLP.md)   
 [CDC::HIMETRICtoLP](../vs140/CDC--HIMETRICtoLP.md)   
 [LPtoDP](http://msdn.microsoft.com/library/windows/desktop/dd145042)   
 [CDC::GetWindowOrg](../vs140/CDC--GetWindowOrg.md)   
 [CDC::GetWindowExt](../vs140/CDC--GetWindowExt.md)