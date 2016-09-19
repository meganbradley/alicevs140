---
title: "CMFCBaseTabCtrl::SetActiveTabTextColor"
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
ms.assetid: d8d5a240-ec5e-417d-935b-cbe2e7b6cda6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetActiveTabTextColor
Sets the text color for active tabs.  
  
## Syntax  
  
```  
virtual void SetActiveTabTextColor(  
   COLORREF clr   
);  
```  
  
#### Parameters  
 [in] `clr`  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that specifies the new text color.  
  
## Remarks  
 By default, the framework obtains the text color from [GetSysColor](http://msdn.microsoft.com/library/windows/desktop/ms724371). Override this default color by using the `SetActiveTabTextColor` method.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::GetActiveTabTextColor](../vs140/CMFCBaseTabCtrl--GetActiveTabTextColor.md)