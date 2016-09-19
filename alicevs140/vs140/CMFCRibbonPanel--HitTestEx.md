---
title: "CMFCRibbonPanel::HitTestEx"
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
ms.assetid: 816d1bea-eb20-4f7c-ab38-2defa9c0ee47
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::HitTestEx
Retrieves the zero-based index of the ribbon element that has the specified point located in it.  
  
## Syntax  
  
```  
virtual int HitTestEx(  
   CPoint point  
) const;  
```  
  
#### Parameters  
 [in] `point`  
 The x and y coordinates of the pointer, relative to the upper-left corner of the window.  
  
## Return Value  
 The zero-based index of the ribbon element that has the specified point located in it; otherwise -1.  
  
## Remarks  
 Only ribbon elements that are contained in the ribbon panel are tested.  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)