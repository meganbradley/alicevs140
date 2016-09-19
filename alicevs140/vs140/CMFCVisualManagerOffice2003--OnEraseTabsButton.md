---
title: "CMFCVisualManagerOffice2003::OnEraseTabsButton"
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
ms.assetid: b07b6551-107e-4545-b3b1-90471d956919
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnEraseTabsButton
The framework calls this method when it erases the text and icon of a tab button.  
  
## Syntax  
  
```  
virtual void OnEraseTabsButton(  
   CDC* pDC,  
   CRect rect,  
   CMFCButton* pButton,  
   CMFCBaseTabCtrl* pWndTab  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the tab button.  
  
 [in] `pButton`  
 A pointer to a tab button. The framework erases the text and icon for this button.  
  
 [in] `pWndTab`  
 A pointer to the tab control that contains the tab button.  
  
## Remarks  
 The framework erases the text and icon for a button when a [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object processes the `WM_ERASEBKGND` message  
  
 Override this method in a derived visual manager to customize the appearance of tab buttons.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)