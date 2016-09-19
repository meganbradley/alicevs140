---
title: "CMFCRibbonCategory::OnLButtonDown"
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
ms.assetid: 5a0c59f8-3c24-4ca0-a4a0-23028cf45c5c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::OnLButtonDown
Called by the framework to retrieve the ribbon element under the specified point when the user presses the left mouse button.  
  
## Syntax  
  
```  
virtual CMFCRibbonBaseElement* OnLButtonDown(  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `point`  
 The x and y coordinates of the mouse pointer, relative to the upper-left corner of the window.  
  
## Return Value  
 Pointer to a ribbon element if the method was successful; otherwise `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)