---
title: "CBasePane::CreateEx"
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
ms.assetid: 6196c8e8-89a7-4960-9044-cac9e4c5f41c
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CreateEx
Creates the pane control.  
  
## Syntax  
  
```  
virtual BOOL CreateEx(  
   DWORD dwStyleEx,  
   LPCTSTR lpszClassName,  
   LPCTSTR lpszWindowName,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID,  
   DWORD dwControlBarStyle=0,  
   CCreateContext* pContext=NULL   
);  
```  
  
#### Parameters  
 [in] `dwStyleEx`  
 The extended styles (see [CWnd::CreateEx](../vs140/CWnd--CreateEx.md) for more information).  
  
 [in] `lpszClassName`  
 The window class name.  
  
 [in] `lpszWindowName`  
 The window name.  
  
 [in] `dwStyle`  
 The window style (see [CWnd::CreateEx](../vs140/CWnd--CreateEx.md)).  
  
 [in] `rect`  
 The initial rectangle.  
  
 [in] `pParentWnd`  
 A pointer to the parent window.  
  
 [in] `nID`  
 Specifies the pane ID. Must be unique.  
  
 [in] `dwControlBarStyle`  
 Style flags for panes.  
  
 [in] `pContext`  
 A pointer to `CcreateContext`  
  
## Return Value  
 `TRUE` if the pane is created successfully; otherwise `FALSE`.  
  
## Remarks  
 Creates a window of class `lpszClassName`. If you specify `WS_CAPTION`, this method clears the `WS_CAPTION` style bit and sets `CBasePane::m_bHasCaption` to `TRUE`, because the library does not support panes with captions.  
  
 You can use any combination of child window styles and MFC control bar (CBRS_) styles.  
  
 The library adds several new styles for panes. The following table describes the new styles:  
  
|Style|Description|  
|-----------|-----------------|  
|`AFX_CBRS_FLOAT`|The pane can float.|  
|`AFX_CBRS_AUTOHIDE`|The pane supports auto-hide mode|  
|`AFX_CBRS_RESIZE`|The pane can be resized. **Important:**  This style is not implemented.|  
|`AFX_CBRS_CLOSE`|The pane can be closed.|  
|`AFX_CBRS_AUTO_ROLLUP`|The pane can be rolled up when it floats.|  
|`AFX_CBRS_REGULAR_TABS`|When one pane docks to another pane that has this style, a regular tabbed window is created. (For more information, see [CTabbedPane Class](../vs140/CTabbedPane-Class.md).)|  
|`AFX_CBRS_OUTLOOK_TABS`|When one pane docks to another pane that has this style, an Outlook-style tabbed window is created. (For more information, see [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md).)|  
  
 To use the new styles, specify them in `dwControlBarStyle`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)