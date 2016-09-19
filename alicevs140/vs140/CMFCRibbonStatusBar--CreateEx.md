---
title: "CMFCRibbonStatusBar::CreateEx"
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
ms.assetid: b82c3212-bc84-418b-96cd-23f49200a528
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::CreateEx
Creates a ribbon status bar that has an extended style.  
  
## Syntax  
  
```  
BOOL CreateEx(  
   CWnd* pParentWnd,  
   DWORD dwCtrlStyle=0,  
   DWORD dwStyle=WS_CHILD|WS_VISIBLE|CBRS_BOTTOM,  
   UINT nID=AFX_IDW_STATUS_BAR   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 A pointer to the parent window.  
  
 `dwCtrlStyle`  
 A logical OR combination of additional styles for creating the status bar object.  
  
 `dwStyle`  
 The control style of the status bar.  
  
 `nID`  
 The control ID of the status bar.  
  
## Return Value  
 `TRUE` if the status bar is created successfully, `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)