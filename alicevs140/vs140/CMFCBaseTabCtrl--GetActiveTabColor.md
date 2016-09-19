---
title: "CMFCBaseTabCtrl::GetActiveTabColor"
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
ms.assetid: d76cd81b-4df7-4ed8-93d6-3ff9dc22b795
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetActiveTabColor
Retrieves the background color of the currently active tab.  
  
## Syntax  
  
```  
virtual COLORREF GetActiveTabColor() const;  
```  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that specifies the background color of the active tab.  
  
## Remarks  
 By default, the background color of the active tab is `COLOR_WINDOW`. You can change the background color for the active tab by using the method [CMFCBaseTabCtrl::SetActiveTabColor](../vs140/CMFCBaseTabCtrl--SetActiveTabColor.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::SetActiveTabColor](../vs140/CMFCBaseTabCtrl--SetActiveTabColor.md)