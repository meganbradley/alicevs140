---
title: "CMFCOutlookBarTabCtrl::AddControl"
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
ms.assetid: 60a81e73-5ce3-4028-a1af-59d1a9c6957d
caps.latest.revision: 22
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::AddControl
Adds a Windows control as a new tab in the Outlook bar.  
  
## Syntax  
  
```  
void AddControl(  
   CWnd* pWndCtrl,  
   LPCTSTR lpszName,  
   int nImageID=-1,  
   BOOL bDetachable=TRUE,  
   DWORD dwControlBarStyle=AFX_CBRS_FLOAT | AFX_CBRS_CLOSE |  
                           AFX_CBRS_RESIZE | CBRS_AFX_AUTOHIDE   
);  
```  
  
#### Parameters  
 [in] `pWndCtrl`  
 A pointer to a control to add.  
  
 [in] `lpszName`  
 Specifies the name of tab.  
  
 [in] `bDetachable`  
 If `TRUE`, the page will be created as detachable.  
  
 [in] `nImageID`  
 Image index in the internal image list for the image to be displayed in the new tab.  
  
 [in] `dwControlBarStyle`  
 Specifies the AFX_`CBRS_`* style for wrapped docking panes.  
  
## Remarks  
 Use this function to add a control as a new page of an outlook bar.  
  
 This function internally calls on [CMFCBaseTabCtrl::AddTab](../vs140/CMFCBaseTabCtrl--AddTab.md).  
  
 If you set `bDetachable` to `TRUE`, `AddControl` internally creates a `CDockablePaneAdapter` object and wraps the added control. It automatically sets the runtime class of the tabbed window to the runtime class of `CMFCOutlookBar` and the runtime class of the floating frame to `CMultiPaneFrameWnd`.  
  
## Example  
 The following example demonstrates how to use the `AddControl` method in the `CMFCOutlookBarTabCtrl` class. This code snippet is part of the [Outlook Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_OutlookDemo#3](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_OutlookDemo#3)]  
  
## Requirements  
 **Header:** afxOutlookBarTabCtrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCOutlookBar](../vs140/CMFCOutlookBar-Class.md)   
 [CMultiPaneFrameWnd](../vs140/CMultiPaneFrameWnd-Class.md)