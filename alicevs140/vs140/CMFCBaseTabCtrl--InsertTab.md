---
title: "CMFCBaseTabCtrl::InsertTab"
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
ms.assetid: 0d1c6692-16a8-42b4-8239-6c652f7310de
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::InsertTab
Inserts a tab into the tab control.  
  
## Syntax  
  
```  
Virtual void InsertTab(  
   CWnd* pNewWnd,  
   LPCTSTR lpszTabLabel,  
   int nInsertAt,  
   UINT uiImageId = (UINT)-1,  
   BOOL bDetachable = TRUE  
);  
virtual void InsertTab(  
   CWnd* pNewWnd,  
   UINT uiResTabLabel,  
   int nInsertAt,  
   UINT uiImageId = (UINT)-1,  
   BOOL bDetachable = TRUE  
);  
```  
  
#### Parameters  
 [in] `pNewWnd`  
 A pointer to the window that this method adds as a new tab.  
  
 [in] `lpszTabLabel`  
 A string that contains the label for the new tab.  
  
 [in] `nInsertAt`  
 The zero-based index of the new tab.  
  
 [in] `uiImageId`  
 An image ID from the image list. The tab control uses this image as the icon for the new tab.  
  
 [in] `bDetachable`  
 A Boolean parameter that determines whether the new tab is detachable.  
  
 [in] `uiResTabLabel`  
 The resource ID for the label.  
  
## Remarks  
 If the object indicated by `pNewWnd` is not derived from the [CDockablePane Class](../vs140/CDockablePane-Class.md) and if the `bDetachable` parameter is `TRUE`, the framework creates a special wrapper for the new tab. By default, the wrapper is an instance of the [CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md). Use the [CMFCBaseTabCtrl::SetDockingBarWrapperRTC](../vs140/CMFCBaseTabCtrl--SetDockingBarWrapperRTC.md) method to create a different wrapper class. Any custom wrapper class needs to be derived from `CDockablePaneAdapter`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md)   
 [CMFCBaseTabCtrl::SetDockingBarWrapperRTC](../vs140/CMFCBaseTabCtrl--SetDockingBarWrapperRTC.md)