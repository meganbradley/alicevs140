---
title: "CMFCBaseTabCtrl::GetTabFromHwnd"
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
ms.assetid: 6582aafd-dc37-488f-92b0-ddd959f7d538
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabFromHwnd
Retrieves the index of the tab that contains the specified HWND object.  
  
## Syntax  
  
```  
virtual int GetTabFromHwnd(  
   HWND hwnd  
) const;  
```  
  
#### Parameters  
 [in] `hwnd`  
 A handle to a window.  
  
## Return Value  
 The zero-based index of the tab if successful; -1 if no tab contains `hwnd`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)