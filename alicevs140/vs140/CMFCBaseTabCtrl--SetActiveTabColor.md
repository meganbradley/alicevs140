---
title: "CMFCBaseTabCtrl::SetActiveTabColor"
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
ms.assetid: a50b34f4-91ff-4aa7-9e6d-3a7d76de69b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetActiveTabColor
Sets the background color for the active tab.  
  
## Syntax  
  
```  
virtual void SetActiveTabColor(  
   COLORREF clr  
);  
```  
  
#### Parameters  
 [in] `clr`  
 Specifies the new background color.  
  
## Remarks  
 The framework obtains the default background color for active tabs from the [GetSysColor](http://msdn.microsoft.com/library/windows/desktop/ms724371)method.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::GetActiveTabColor](../vs140/CMFCBaseTabCtrl--GetActiveTabColor.md)