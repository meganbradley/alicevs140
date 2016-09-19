---
title: "CMFCVisualManager::OnEraseTabsArea"
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
ms.assetid: e2d0c754-b5e1-433b-bc5c-cf43b5de8916
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnEraseTabsArea
The framework calls this method when it erases the tab area of a tab window.  
  
## Syntax  
  
```  
virtual void OnEraseTabsArea(  
   CDC* pDC,  
   CRect rect,  
   const CMFCBaseTabCtrl* pTabWnd  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the tab area.  
  
 [in] `pTabWnd`  
 A pointer to a tab window. The framework erases the tab area for the specified tab window.  
  
## Remarks  
 This function is called by the framework when a [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md) object processes a `WM_PAINT` message and erases the tab area.  
  
 Override this method in a derived visual manager to customize the appearance of tabs.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)