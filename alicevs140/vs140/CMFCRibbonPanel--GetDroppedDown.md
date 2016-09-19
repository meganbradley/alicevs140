---
title: "CMFCRibbonPanel::GetDroppedDown"
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
ms.assetid: a397cc46-292b-40da-891c-234be1d01bf1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::GetDroppedDown
Retrieves a pointer to a ribbon element if its pop-up menu is dropped down.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* GetDroppedDown() const;  
```  
  
## Return Value  
 Pointer to the ribbon element that has its pop-up menu dropped down; otherwise `NULL` if no ribbon element has its pop-up menu dropped down.  
  
## Remarks  
 Only ribbon elements that are contained in the ribbon panel are tested.  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)