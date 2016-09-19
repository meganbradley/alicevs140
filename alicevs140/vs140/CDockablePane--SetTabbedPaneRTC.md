---
title: "CDockablePane::SetTabbedPaneRTC"
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
ms.assetid: cc33e8c0-fd65-4f18-a4d0-3075e6ca9553
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::SetTabbedPaneRTC
Sets the runtime class information for a tabbed window that is created when two panes dock together.  
  
## Syntax  
  
```  
void SetTabbedPaneRTC(  
    CRuntimeClass* pRTC  
);  
```  
  
#### Parameters  
 [in] `pRTC`  
 The runtime class information for the tabbed pane.  
  
## Remarks  
 Call this method to set the runtime class information for tabbed panes that are created dynamically. This can occur when a user drags one pane to the caption of another pane, or if you call the [CDockablePane::AttachToTabWnd](../vs140/CDockablePane--AttachToTabWnd.md) method to programmatically create a tabbed pane from two dockable panes.  
  
 The default runtime class is set according to the `dwTabbedStyle` parameter of [CDockablePane::Create](../vs140/CDockablePane--Create.md) and [CDockablePane::CreateEx](../vs140/CDockablePane--CreateEx.md). To customize the new tabbed panes, derive your class from one of the following classes:  
  
-   [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)  
  
-   [CTabbedPane Class](../vs140/CTabbedPane-Class.md)  
  
-   [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md).  
  
 Then, call this method with the pointer to its runtime class information.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)