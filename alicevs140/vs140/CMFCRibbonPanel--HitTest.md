---
title: "CMFCRibbonPanel::HitTest"
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
ms.assetid: 79d0c2d8-fcbc-4a60-8d87-866918d576f1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::HitTest
Retrieves a ribbon element if the specified point is located in it.  
  
## Syntax  
  
```  
virtual CMFCRibbonBaseElement* HitTest(  
   CPoint point,  
   BOOL bCheckPanelCaption = FALSE  
);  
```  
  
#### Parameters  
 [in] `point`  
 The x and y coordinates of the pointer, relative to the upper-left corner of the window.  
  
 [in] `bCheckPanelCaption`  
 `TRUE` to test the ribbon panel caption; otherwise `FALSE`.  
  
## Return Value  
 Pointer to a ribbon element if the specified point is located in it; otherwise `NULL`.  
  
## Remarks  
 Only ribbon elements that are contained in the ribbon panel are tested.  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)