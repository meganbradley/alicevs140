---
title: "CMFCVisualManagerOffice2003::OnDrawTabsButtonBorder"
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
ms.assetid: b3f224dc-d97d-4d5c-a126-eced51ba00e0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawTabsButtonBorder
The framework calls this method when it draws the border of a tab button.  
  
## Syntax  
  
```  
virtual void OnDrawTabsButtonBorder(  
   CDC* pDC,  
   CRect& rect,  
   CMFCButton* pButton,  
   UINT uiState,  
   CMFCBaseTabCtrl* pWndTab  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the tab button.  
  
 [in] `pButton`  
 A pointer to the [CMFCButton](../vs140/CMFCButton-Class.md) for which the framework draws the border.  
  
 [in] `uiState`  
 The state of the button (see [CButton::GetState](../vs140/CButton--GetState.md)).  
  
 [in] `pWndTab`  
 A pointer to the parent tab window.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the border of the tab button.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)