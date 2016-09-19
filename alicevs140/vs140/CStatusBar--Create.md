---
title: "CStatusBar::Create"
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
ms.assetid: ca67ec4d-91dd-41b8-bc1f-58fc822e8591
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::Create
Creates a status bar (a child window) and associates it with the `CStatusBar` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle = WS_CHILD | WS_VISIBLE | CBRS_BOTTOM,  
   UINT nID = AFX_IDW_STATUS_BAR   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 Pointer to the [CWnd](../vs140/CWnd-Class.md) object whose Windows window is the parent of the status bar.  
  
 `dwStyle`  
 The status-bar style. In addition to the standard Windows [styles](../vs140/Window-Styles.md), these styles are supported.  
  
-   `CBRS_TOP` Control bar is at top of frame window.  
  
-   `CBRS_BOTTOM` Control bar is at bottom of frame window.  
  
-   `CBRS_NOALIGN` Control bar is not repositioned when the parent is resized.  
  
 `nID`  
 The toolbar's child-window ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Also sets the initial font and sets the status bar's height to a default value.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::SetIndicators](../vs140/CStatusBar--SetIndicators.md)