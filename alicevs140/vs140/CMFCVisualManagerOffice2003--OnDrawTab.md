---
title: "CMFCVisualManagerOffice2003::OnDrawTab"
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
ms.assetid: d5590dbf-bbae-495e-b5fa-4f7f3248f2cd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawTab
The framework calls this method when it draws the tabs for a [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnDrawTab(  
   CDC* pDC,  
   CRect rectTab,  
   int iTab,  
   BOOL bIsActive,  
   const CMFCBaseTabCtrl* pTabWnd  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectTab`  
 A rectangle that specifies the boundaries of the tab control.  
  
 [in] `iTab`  
 The index of the tab that the framework draws.  
  
 [in] `bIsActive`  
 A Boolean parameter that specifies whether the tab is active.  
  
 [in] `pTabWnd`  
 A pointer to a [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object. The framework draws this tab control.  
  
## Remarks  
 A `CMFCBaseTabCtrl` object calls this method when it processes the `WM_PAINT` message.Override this method in a derived class to customize the look of tabs.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)