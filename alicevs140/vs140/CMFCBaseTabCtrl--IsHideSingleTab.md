---
title: "CMFCBaseTabCtrl::IsHideSingleTab"
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
ms.assetid: c5a65eda-5be4-4171-9491-722fc195e321
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::IsHideSingleTab
Determines whether the tab control hides the tab label if there is only one tab.  
  
## Syntax  
  
```  
virtual BOOL IsHideSingleTab() const;  
```  
  
## Return Value  
 `TRUE` if the tab control hides the tab label when it has one tab; otherwise `FALSE`.  
  
## Remarks  
 Use the method [CMFCBaseTabCtrl::HideSingleTab](../vs140/CMFCBaseTabCtrl--HideSingleTab.md) to enable hiding the tab label when there is only one tab.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::HideSingleTab](../vs140/CMFCBaseTabCtrl--HideSingleTab.md)