---
title: "CMFCVisualManagerOffice2003::OnFillTab"
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
ms.assetid: e734822f-be3f-444a-828e-ab9193c4b943
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnFillTab
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
 A pointer to the brush that the framework is using to fill the tab window.  
  
 [in] `iTab`  
 The zero-based tab index of a tab for which the framework fills the background.  
  
 [in] `bIsActive`  
 `TRUE` if the tab is active or `FALSE` if not.  
  
 [in] `pTabWnd`  
 A pointer to the parent tab control.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of tabs.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)