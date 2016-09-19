---
title: "CMFCVisualManager::OnEraseTabsFrame"
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
ms.assetid: 1474e208-70c9-4901-aa21-b1cbbc3ac323
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnEraseTabsFrame
The framework calls this method when it erases a frame on a [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md).  
  
## Syntax  
  
```  
virtual BOOL OnEraseTabsFrame(  
   CDC* pDC,  
   CRect rect,  
   const CMFCBaseTabCtrl* pTabWnd  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the tab window.  
  
 [in] `pTabWnd`  
 A pointer to a tab window. The framework erases a frame for this `CMFCBaseTabCtrl`.  
  
## Return Value  
 `TRUE` if the method is successful; `FALSE` otherwise.  
  
## Remarks  
 This method fills the area indicated by `rect` with the background color of the active tab. It is called when a `CMFCBaseTabCtrl` object processes a `WM_PAINT` message and erases a tab frame.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)