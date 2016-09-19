---
title: "CMFCRibbonCategory::GetPanelFromPoint"
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
ms.assetid: e5a304cd-9c3f-48c5-b9b4-6f2482601bf2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::GetPanelFromPoint
Retrieves a pointer to a ribbon panel if the specified point is located in it.  
  
## Syntax  
  
```  
CMFCRibbonPanel* GetPanelFromPoint(  
   CPoint point  
) const;  
```  
  
#### Parameters  
 [in] `point`  
 The x and y coordinates of the pointer, relative to the upper-left corner of the window.  
  
## Return Value  
 Pointer to a ribbon panel if the method was successful; otherwise `NULL`.  
  
## Remarks  
 Only ribbon panels that are contained in the ribbon category are tested.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)