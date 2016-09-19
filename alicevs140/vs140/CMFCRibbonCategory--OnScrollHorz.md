---
title: "CMFCRibbonCategory::OnScrollHorz"
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
ms.assetid: b25831e1-ec2d-4f05-8791-144fb200e628
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::OnScrollHorz
Scrolls the ribbon category in the horizontal direction.  
  
## Syntax  
  
```  
virtual BOOL OnScrollHorz(  
   BOOL bScrollLeft,  
   int nScrollOffset = 0  
);  
```  
  
#### Parameters  
 [in] `bScrollLeft`  
 `TRUE` to scroll to the left; `FALSE` to scroll to the right.  
  
 [in] `nScrollOffset`  
 The scroll distance in pixels.  
  
## Return Value  
 `TRUE` if the ribbon category moved in a horizontal direction; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)