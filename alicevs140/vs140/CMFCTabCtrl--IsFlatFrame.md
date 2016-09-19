---
title: "CMFCTabCtrl::IsFlatFrame"
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
ms.assetid: fc9af7d0-ab90-4754-af93-3458a4dc4891
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::IsFlatFrame
Indicates whether the frame around the tab area is flat or 3D.  
  
## Syntax  
  
```  
BOOL IsFlatFrame() const;  
```  
  
## Return Value  
 `TRUE` if the frame around the tab area is flat; `FALSE` if the frame is three-dimensional.  
  
## Remarks  
 Use the [CMFCTabCtrl::SetFlatFrame](../vs140/CMFCTabCtrl--SetFlatFrame.md) method to change how the frame is drawn.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTabCtrl::SetFlatFrame](../vs140/CMFCTabCtrl--SetFlatFrame.md)