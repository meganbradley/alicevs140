---
title: "CMDIFrameWndEx::OnShowCustomizePane"
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
ms.assetid: c37aaf3d-0194-4d9f-9137-2cdf5d62db20
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnShowCustomizePane
Called by the framework when a Quick Customize pane is activated.  
  
## Syntax  
  
```  
virtual BOOL OnShowCustomizePane(  
   CMFCPopupMenu* pMenuPane,  
   UINT uiToolbarID   
);  
```  
  
#### Parameters  
 [in] `pMenuPane`  
 A pointer to the Quick Customize pane.  
  
 [in] `uiToolbarID`  
 Control ID of the toolbar to customize.  
  
## Return Value  
 This method always returns `TRUE`.  
  
## Remarks  
 The Quick Customize pane is a menu that opens when the user clicks **Customize** on a toolbar.  
  
 Override this method in a derived class to make changes in the Quick Customize pane.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)