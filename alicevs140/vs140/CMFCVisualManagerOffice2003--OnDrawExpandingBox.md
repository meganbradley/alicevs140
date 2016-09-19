---
title: "CMFCVisualManagerOffice2003::OnDrawExpandingBox"
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
ms.assetid: 9ba93a88-9fb1-40f4-955c-379d0ecaec1f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawExpandingBox
Called by the framework while drawing an expanding box.  
  
## Syntax  
  
```  
virtual void OnDrawExpandingBox(  
   CDC* pDC,  
   CRect rect,  
   BOOL bIsOpened,  
   COLORREF colorBox  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the display context in which the expanding box is to be drawn.  
  
 [in] `rect`  
 The bounding rectangle of the expanding box to be drawn.  
  
 [in] `bIsOpened`  
 `TRUE` if the box to be drawn is opened, or `FALSE` if not.  
  
 [in] `colorBox`  
 The color of the outside border of the box to be drawn.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)