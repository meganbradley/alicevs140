---
title: "CMFCVisualManager::OnEraseTabsButton"
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
ms.assetid: 01e001cd-e48c-41ee-8265-63bbc7bfdcf2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnEraseTabsButton
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
 The framework erases the text and icon for a button when a [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object processes the `WM_ERASEBKGND` message.  
  
 Override this method in a derived visual manager to customize the appearance of tab buttons.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)