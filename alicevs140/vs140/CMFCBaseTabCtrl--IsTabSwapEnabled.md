---
title: "CMFCBaseTabCtrl::IsTabSwapEnabled"
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
ms.assetid: e0f52851-f477-48a5-a36a-397ebc5cc6ec
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::IsTabSwapEnabled
Determines whether the tab control allows the user to change tab positions by using the mouse.  
  
## Syntax  
  
```  
BOOL IsTabSwapEnabled() const;  
```  
  
## Return Value  
 Nonzero if tab positions can be changed by the user; otherwise 0.  
  
## Remarks  
 By default, users cannot change the order of tabs in a tab control. Use the [CMFCBaseTabCtrl::EnableTabSwap](../vs140/CMFCBaseTabCtrl--EnableTabSwap.md) method to enable this functionality.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::EnableTabSwap](../vs140/CMFCBaseTabCtrl--EnableTabSwap.md)