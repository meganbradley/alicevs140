---
title: "CDC::OffsetViewportOrg"
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
ms.assetid: 784c6724-73e9-46fa-9c75-aa040f00af0b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::OffsetViewportOrg
Modifies the coordinates of the viewport origin relative to the coordinates of the current viewport origin.  
  
## Syntax  
  
```  
  
      virtual CPoint OffsetViewportOrg(  
   int nWidth,  
   int nHeight   
);  
```  
  
#### Parameters  
 `nWidth`  
 Specifies the number of device units to add to the current origin's x-coordinate.  
  
 `nHeight`  
 Specifies the number of device units to add to the current origin's y-coordinate.  
  
## Return Value  
 The previous viewport origin (in device coordinates) as a `CPoint` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetViewportOrg](../vs140/CDC--GetViewportOrg.md)   
 [CDC::OffsetWindowOrg](../vs140/CDC--OffsetWindowOrg.md)   
 [CDC::SetViewportOrg](../vs140/CDC--SetViewportOrg.md)   
 [CPoint Class](../vs140/CPoint-Class.md)