---
title: "CDC::OffsetWindowOrg"
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
ms.assetid: 220b2e48-3a18-4828-bc2d-6dba103a5c34
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::OffsetWindowOrg
Modifies the coordinates of the window origin relative to the coordinates of the current window origin.  
  
## Syntax  
  
```  
  
      CPoint OffsetWindowOrg(  
   int nWidth,  
   int nHeight   
);  
```  
  
#### Parameters  
 `nWidth`  
 Specifies the number of logical units to add to the current origin's x-coordinate.  
  
 `nHeight`  
 Specifies the number of logical units to add to the current origin's y-coordinate.  
  
## Return Value  
 The previous window origin (in logical coordinates) as a `CPoint` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetWindowOrg](../vs140/CDC--GetWindowOrg.md)   
 [CDC::OffsetViewportOrg](../vs140/CDC--OffsetViewportOrg.md)   
 [CDC::SetWindowOrg](../vs140/CDC--SetWindowOrg.md)   
 [CPoint Class](../vs140/CPoint-Class.md)