---
title: "CSplitterWnd::CreateStatic"
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
ms.assetid: d3f22381-146f-4080-8aa3-3d5dba6223dd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::CreateStatic
To create a static splitter window, call the `CreateStatic` member function.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateStatic(  
   CWnd* pParentWnd,  
   int nRows,  
   int nCols,  
   DWORD dwStyle = WS_CHILD | WS_VISIBLE,  
   UINT nID = AFX_IDW_PANE_FIRST   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 The parent frame window of the splitter window.  
  
 `nRows`  
 The number of rows. This value must not exceed 16.  
  
 *nCols*  
 The number of columns. This value must not exceed 16.  
  
 `dwStyle`  
 Specifies the window style.  
  
 `nID`  
 The child window ID of the window. The ID can be **AFX_IDW_PANE_FIRST** unless the splitter window is nested inside another splitter window.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 A `CSplitterWnd` is usually embedded in a parent `CFrameWnd` or [CMDIChildWnd](../vs140/CMDIChildWnd-Class.md) object by taking the following steps:  
  
1.  Embed a `CSplitterWnd` member variable in the parent frame.  
  
2.  Override the parent frame's `OnCreateClient` member function.  
  
3.  Call the `CreateStatic` member function from within the overridden [CFrameWnd::OnCreateClient](../vs140/CFrameWnd--OnCreateClient.md).  
  
 A static splitter window contains a fixed number of panes, often from different classes.  
  
 When you create a static splitter window, you must at the same time create all its panes. The [CreateView](../vs140/CSplitterWnd--CreateView.md) member function is usually used for this purpose, but you can create other nonview classes as well.  
  
 The initial minimum row height and column width for a static splitter window is 0. These minimums, which determine when a pane is too small to be shown in its entirety, can be changed with the [SetRowInfo](../vs140/CSplitterWnd--SetRowInfo.md) and [SetColumnInfo](../vs140/CSplitterWnd--SetColumnInfo.md) member functions.  
  
 To add scroll bars to a static splitter window, add the **WS_HSCROLL** and **WS_VSCROLL** styles to `dwStyle`.  
  
 See "Splitter Windows" in the article [Multiple Document Types, Views, and Frame Windows](../vs140/Multiple-Document-Types--Views--and-Frame-Windows.md), [Technical Note 29](../vs140/TN029--Splitter-Windows.md), and the [CSplitterWnd](../vs140/CSplitterWnd-Class.md) class overview for more on static splitter windows.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::Create](../vs140/CSplitterWnd--Create.md)   
 [CFrameWnd::OnCreateClient](../vs140/CFrameWnd--OnCreateClient.md)   
 [CSplitterWnd::SetRowInfo](../vs140/CSplitterWnd--SetRowInfo.md)   
 [CSplitterWnd::SetColumnInfo](../vs140/CSplitterWnd--SetColumnInfo.md)   
 [CSplitterWnd::CreateView](../vs140/CSplitterWnd--CreateView.md)