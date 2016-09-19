---
title: "CMFCVisualManager::OnFillTab"
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
ms.assetid: da896cc0-fc00-495e-89b8-323b3fb0026d
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillTab
The framework calls this method when it fills the background of a tab window.  
  
## Syntax  
  
```  
virtual void OnFillTab(  
   CDC* pDC,  
   CRect rectFill,  
   CBrush* pbrFill,  
   int iTab,  
   BOOL bIsActive,  
   const CMFCBaseTabCtrl* pTabWnd  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectFill`  
 A rectangle that specifies the boundaries for the tab window.  
  
 [in] `pbrFill`  
 A pointer to a brush. The framework uses this brush to fill the tab window.  
  
 [in] `iTab`  
 The zero-based tab index of a tab for which the framework fills the background.  
  
 [in] `bIsActive`  
 `TRUE` if the tab is active; otherwise `FALSE`.  
  
 [in] `pTabWnd`  
 A pointer to the parent tab control.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of tabs.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)