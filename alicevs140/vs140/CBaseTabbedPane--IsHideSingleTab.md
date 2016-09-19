---
title: "CBaseTabbedPane::IsHideSingleTab"
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
ms.assetid: eab19c36-2b0f-448f-8322-f8411c4e5c62
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::IsHideSingleTab
Determines whether the tabbed pane is hidden if only one tab is displayed.  
  
## Syntax  
  
```  
virtual BOOL IsHideSingleTab() const;  
```  
  
## Return Value  
 `TRUE` if the tab window is not shown when there is only one visible tab; otherwise, `FALSE`.  
  
## Remarks  
 If the pane is not displayed because only one tab is open, you can call this method to determine whether the tabbed pane is working correctly.  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)