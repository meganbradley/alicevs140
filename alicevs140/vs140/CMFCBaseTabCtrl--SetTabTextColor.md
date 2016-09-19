---
title: "CMFCBaseTabCtrl::SetTabTextColor"
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
ms.assetid: 5367522e-2c96-4c8d-b203-194474071479
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetTabTextColor
Sets the text color for a specific tab.  
  
## Syntax  
  
```  
virtual BOOL SetTabTextColor(  
   int iTab,  
   COLORREF color = (COLORREF)-1  
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab.  
  
 [in] `color`  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that indicates the new text color.  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::GetTabTextColor](../vs140/CMFCBaseTabCtrl--GetTabTextColor.md)