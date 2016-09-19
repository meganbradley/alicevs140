---
title: "CMFCTabCtrl::SetActiveTab"
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
ms.assetid: eb59aebd-74b9-4ffd-9d5e-ca6a7d6c667f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::SetActiveTab
Activates a tab.  
  
## Syntax  
  
```  
virtual BOOL SetActiveTab(  
   int iTab   
);  
```  
  
#### Parameters  
 [in] `iTab`  
 Specifies the zero-based index of the tab to activate.  
  
## Return Value  
 `TRUE` if the specified tab was made active; `FALSE` if the specified `iTab` parameter value is invalid.  
  
## Remarks  
 This method does not send the `AFX_WM_CHANGE_ACTIVE_TAB` notification to the parent window of the tab control.  
  
 The `SetActiveTab` method automatically calls the [CMFCTabCtrl::HideActiveWindowHorzScrollBar](../vs140/CMFCTabCtrl--HideActiveWindowHorzScrollBar.md) method to prevent the screen from blinking.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)