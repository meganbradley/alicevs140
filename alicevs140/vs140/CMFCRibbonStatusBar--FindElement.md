---
title: "CMFCRibbonStatusBar::FindElement"
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
ms.assetid: ba2d6d6d-408e-4919-98ba-c11c9f8ea5e7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::FindElement
Returns a pointer to the element that has the specified command ID.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* FindElement(  
   UINT uiID   
);  
```  
  
#### Parameters  
 [in] `uiID`  
 The ID of the element.  
  
## Return Value  
 A pointer to the element that has the specified command ID. `NULL` if there is no such element.  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)