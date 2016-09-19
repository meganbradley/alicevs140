---
title: "CMFCBaseTabCtrl::RemoveTab"
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
ms.assetid: 36461f6b-0da1-4965-a967-37f3d7cea75d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::RemoveTab
Removes a tab from the tab control.  
  
## Syntax  
  
```  
virtual BOOL RemoveTab(  
   int iTab,  
   BOOL bRecalcLayout = TRUE  
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of a tab.  
  
 [in] `bRecalcLayout`  
 A Boolean parameter that specifies whether to recalculate the layout of the tab.  
  
## Return Value  
 `TRUE` if the method removes the tab successfully; otherwise `FALSE`.  
  
## Remarks  
 If [CMFCBaseTabCtrl::m_bAutoDestroyWindow](../vs140/CMFCBaseTabCtrl--m_bAutoDestroyWindow.md) is `TRUE`, `RemoveTab` destroys the [CWnd](../vs140/CWnd-Class.md) object associated with the specified tab.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)