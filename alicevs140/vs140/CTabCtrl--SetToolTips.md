---
title: "CTabCtrl::SetToolTips"
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
ms.assetid: e66d7236-5464-4a32-a72d-93afebc002d6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::SetToolTips
Assigns a tool tip control to a tab control.  
  
## Syntax  
  
```  
  
      void SetToolTips(  
  CToolTipCtrl* pWndTip   
);  
```  
  
#### Parameters  
 `pWndTip`  
 Handle of the tool tip control.  
  
## Remarks  
 You can get the tool tip control associated with a tab control by making a call to `GetToolTips`.  
  
## Example  
 See the example for [CPropertySheet::GetTabControl](../vs140/CPropertySheet--GetTabControl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::GetToolTips](../vs140/CTabCtrl--GetToolTips.md)