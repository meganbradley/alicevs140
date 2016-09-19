---
title: "CMFCVisualManagerWindows7::OnFillMenuImageRect"
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
ms.assetid: fbbdabab-3667-4501-ae04-e1de4a1bd426
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerWindows7::OnFillMenuImageRect
The framework calls this method when it fills area around a menu item image.  
  
## Syntax  
  
```  
virtual void OnFillMenuImageRect(  
   CDC* pDC,  
   CMFCToolBarButton* pButton,  
   CRect rect,  
   CMFCVisualManager::AFX_BUTTON_STATE state  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context of a menu button.  
  
 [in] `pButton`  
 A pointer to a `CMFCToolBarButton`. The framework fills the background for this button.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the menu button image area.  
  
 [in] `state`  
 The button state.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanagerwindows7.h  
  
## See Also  
 [CMFCVisualManagerWindows7 Class](../vs140/CMFCVisualManagerWindows7-Class.md)   
 [](../vs140/CMFCVisualManagerWindows7-Class.md "CMFCVisualManagerWindows7 Class")   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)