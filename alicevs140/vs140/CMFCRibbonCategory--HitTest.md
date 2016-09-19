---
title: "CMFCRibbonCategory::HitTest"
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
ms.assetid: 997c2fb8-d542-49ad-80f4-2405e41985ea
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::HitTest
Retrieves a pointer to a ribbon element if the specified point is located in it.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* HitTest(  
   CPoint point,  
   BOOL bCheckPanelCaption = FALSE  
) const;  
```  
  
#### Parameters  
 [in] `point`  
 The x and y coordinates of the mouse pointer, relative to the upper-left corner of the window.  
  
 [in] `bCheckPanelCaption`  
 `TRUE` to test the ribbon panel caption; `FALSE` to exclude the ribbon panel caption.  
  
## Return Value  
 Pointer to a ribbon element if the method was successful; otherwise `NULL`.  
  
## Remarks  
 Only ribbon elements that are contained in the ribbon category are tested.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)