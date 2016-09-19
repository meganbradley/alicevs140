---
title: "CMFCTabCtrl::StopResize"
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
ms.assetid: e6df6de2-6117-4bdf-9e49-a0c97edf62a4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::StopResize
Terminates the current resize operation on the tab control.  
  
## Syntax  
  
```  
void StopResize(  
   BOOL bCancel  
);  
```  
  
#### Parameters  
 [in] `bCancel`  
 `TRUE` to abandon the current resize operation; `FALSE` to complete the current resize operation. In either case, the framework stops drawing the resize rectangle.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)