---
title: "CDC::DPtoLP"
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
ms.assetid: a2f0ce3a-e775-4646-813d-707a00eb2e0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DPtoLP
Converts device units into logical units.  
  
## Syntax  
  
```  
  
      void DPtoLP(  
   LPPOINT lpPoints,  
   int nCount = 1   
) const;  
void DPtoLP(  
   LPRECT lpRect   
) const;  
void DPtoLP(  
   LPSIZE lpSize   
) const;  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of [POINT](../vs140/POINT-Structure.md) structures or [CPoint](../vs140/CPoint-Class.md) objects.  
  
 `nCount`  
 The number of points in the array.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or [CRect](../vs140/CRect-Class.md) object. This parameter is used for the simple case of converting one rectangle from device points to logical points.  
  
 `lpSize`  
 Points to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object.  
  
## Remarks  
 The function maps the coordinates of each point, or dimension of a size, from the device coordinate system into GDI's logical coordinate system. The conversion depends on the current mapping mode and the settings of the origins and extents for the device's window and viewport.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::LPtoDP](../vs140/CDC--LPtoDP.md)   
 [CDC::HIMETRICtoDP](../vs140/CDC--HIMETRICtoDP.md)   
 [DPtoLP](http://msdn.microsoft.com/library/windows/desktop/dd162474)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [RECT Structure](../vs140/RECT-Structure.md)   
 [CDC::GetWindowExt](../vs140/CDC--GetWindowExt.md)   
 [CDC::GetWindowOrg](../vs140/CDC--GetWindowOrg.md)