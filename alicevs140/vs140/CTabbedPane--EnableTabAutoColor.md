---
title: "CTabbedPane::EnableTabAutoColor"
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
ms.assetid: 3779f994-5963-41fd-a277-0c811ad36d9f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabbedPane::EnableTabAutoColor
Enables or disables automatic coloring of tabs.  
  
## Syntax  
  
```  
static void EnableTabAutoColor(  
    BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable auto coloring of tabs; otherwise, `FALSE`.  
  
## Remarks  
 Use this static method to enable or disable automatic coloring of tabs in all tabbed panes in the application. When this feature is enabled, each tab is filled by its own color. You can find the list of colors that are used to color the tabs by calling the [CMFCBaseTabCtrl::GetAutoColors](../vs140/CMFCBaseTabCtrl--GetAutoColors.md) method.  
  
 You can specify the list of colors that will be used for tabs by calling [CTabbedPane::SetTabAutoColors](../vs140/CTabbedPane--SetTabAutoColors.md).  
  
 By default, this option is disabled.  
  
## Requirements  
 **Header:** afxTabbedPane.h  
  
## See Also  
 [CTabbedPane Class](../vs140/CTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)