---
title: "CMFCListCtrl::EnableMarkSortedColumn"
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
ms.assetid: 7e216e5d-0669-471f-ac16-9efe6c3dbe4b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::EnableMarkSortedColumn
Marks the sorted columns with a different background color.  
  
## Syntax  
  
```  
void EnableMarkSortedColumn(  
   BOOL bMark = TRUE,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 [in] `bMark`  
 A Boolean parameter that determines whether to enable a different background color.  
  
 [in] `bRedraw`  
 A Boolean parameter that determines whether to redraw the control immediately.  
  
## Remarks  
 `EnableMarkSortedColumn` uses the method `CDrawingManager::PixelAlpha` to calculate what color to use for sorted columns. The color picked is based upon the regular background color.  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)