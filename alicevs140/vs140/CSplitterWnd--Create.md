---
title: "CSplitterWnd::Create"
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
ms.assetid: fe64c958-e4c5-4225-9943-d289bbf673c2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::Create
To create a dynamic splitter window, call the **Create** member function.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd,  
   int nMaxRows,  
   int nMaxCols,  
   SIZE sizeMin,  
   CCreateContext* pContext,  
   DWORD dwStyle = WS_CHILD | WS_VISIBLE | WS_HSCROLL | WS_VSCROLL | SPLS_DYNAMIC_SPLIT,  
   UINT nID = AFX_IDW_PANE_FIRST   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 The parent frame window of the splitter window.  
  
 *nMaxRows*  
 The maximum number of rows in the splitter window. This value must not exceed 2.  
  
 *nMaxCols*  
 The maximum number of columns in the splitter window. This value must not exceed 2.  
  
 `sizeMin`  
 Specifies the minimum size at which a pane may be displayed.  
  
 `pContext`  
 A pointer to a [CCreateContext](../vs140/CCreateContext-Structure.md) structure. In most cases, this can be the `pContext` passed to the parent frame window.  
  
 `dwStyle`  
 Specifies the window style.  
  
 `nID`  
 The child window ID of the window. The ID can be **AFX_IDW_PANE_FIRST** unless the splitter window is nested inside another splitter window.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You can embed a `CSplitterWnd` in a parent [CFrameWnd](../vs140/CFrameWnd-Class.md) or [CMDIChildWnd](../vs140/CMDIChildWnd-Class.md) object by taking the following steps:  
  
1.  Embed a `CSplitterWnd` member variable in the parent frame.  
  
2.  Override the parent frame's [CFrameWnd::OnCreateClient](../vs140/CFrameWnd--OnCreateClient.md) member function.  
  
3.  Call the **Create** member function from within the overridden `OnCreateClient`.  
  
 When you create a splitter window from within a parent frame, pass the parent frame's `pContext` parameter to the splitter window. Otherwise, this parameter can be **NULL**.  
  
 The initial minimum row height and column width of a dynamic splitter window are set by the `sizeMin` parameter. These minimums, which determine whether a pane is too small to be shown in its entirety, can be changed with the [SetRowInfo](../vs140/CSplitterWnd--SetRowInfo.md) and [SetColumnInfo](../vs140/CSplitterWnd--SetColumnInfo.md) member functions.  
  
 For more on dynamic splitter windows, see "Splitter Windows" in the article [Multiple Document Types, Views, and Frame Windows](../vs140/Multiple-Document-Types--Views--and-Frame-Windows.md), [Technical Note 29](../vs140/TN029--Splitter-Windows.md), and the [CSplitterWnd](../vs140/CSplitterWnd-Class.md) class overview.  
  
## Example  
 [!CODE [NVC_MFCWindowing#125](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#125)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::CreateStatic](../vs140/CSplitterWnd--CreateStatic.md)   
 [CFrameWnd::OnCreateClient](../vs140/CFrameWnd--OnCreateClient.md)   
 [CSplitterWnd::SetRowInfo](../vs140/CSplitterWnd--SetRowInfo.md)   
 [CSplitterWnd::SetColumnInfo](../vs140/CSplitterWnd--SetColumnInfo.md)   
 [CSplitterWnd::CreateView](../vs140/CSplitterWnd--CreateView.md)