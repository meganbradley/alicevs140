---
title: "CMFCBaseTabCtrl::GetTabWnd"
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
ms.assetid: c060aac0-0bcb-49bc-b5d6-58784ec69944
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabWnd
Returns the pointer to the pane that resides on the specified tab.  
  
## Syntax  
  
```  
virtual CWnd* GetTabWnd(  
   int iTab   
) const;  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of a tab.  
  
## Return Value  
 A pointer to the [CWnd](../vs140/CWnd-Class.md) object that resides on the tab that `iTab` specifies. `NULL` if `iTab` is invalid.  
  
## Remarks  
 The returned object is the one that the application added when it called either [CMFCBaseTabCtrl::AddTab](../vs140/CMFCBaseTabCtrl--AddTab.md) or [CMFCBaseTabCtrl::InsertTab](../vs140/CMFCBaseTabCtrl--InsertTab.md).  
  
 If the object on a tab has a wrapper, this method will return the wrapper for the object. For more information about wrappers, see [CMFCBaseTabCtrl::CreateWrapper](../vs140/CMFCBaseTabCtrl--CreateWrapper.md). If you want to access a pointer to the direct object without the wrapper, use the method [CMFCBaseTabCtrl::GetTabWndNoWrapper](../vs140/CMFCBaseTabCtrl--GetTabWndNoWrapper.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::GetTabWndNoWrapper](../vs140/CMFCBaseTabCtrl--GetTabWndNoWrapper.md)