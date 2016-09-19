---
title: "CMFCVisualManager::OnDrawTearOffCaption"
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
ms.assetid: 429f9af3-9579-4cab-a81e-f8fc121e2f94
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawTearOffCaption
The framework calls this method when it draws the caption for a [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawTearOffCaption(  
   CDC* pDC,  
   CRect rect,  
   BOOL bIsActive  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the caption.  
  
 [in] `bIsActive`  
 `TRUE` if the caption is active; `FALSE` otherwise.  
  
## Remarks  
 This function is called by the framework when a `CMFCPopupMenu` object processes a WM_PAINT message and must draw a tear-off caption.  
  
 Override this method in a derived class to customize the look of captions for tear-off bars.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)