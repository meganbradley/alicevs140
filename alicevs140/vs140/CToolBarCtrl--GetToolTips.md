---
title: "CToolBarCtrl::GetToolTips"
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
ms.assetid: f2cdf90e-dedf-4944-a7cf-6a7b03447916
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetToolTips
Retrieves the handle of the tool tip control, if any, associated with the toolbar control.  
  
## Syntax  
  
```  
  
CToolTipCtrl* GetToolTips( ) const;  
```  
  
## Return Value  
 A pointer to the [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object associated with this toolbar or **NULL** if the toolbar has no associated tool tip control.  
  
## Remarks  
 Since the toolbar control normally creates and maintains its own tool tip control, most programs don't need to call this function.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetToolTips](../vs140/CToolBarCtrl--SetToolTips.md)   
 [Handling Tool Tip Notifications](../vs140/Handling-Tool-Tip-Notifications.md)   
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)