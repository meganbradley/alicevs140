---
title: "CMFCBaseTabCtrl::GetTabByID"
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
ms.assetid: 45b4ca44-0c5a-4f2a-b217-4a8c2d99ce47
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabByID
Retrieves the index of a tab based on a tab ID.  
  
## Syntax  
  
```  
virtual int GetTabByID(  
   int id  
) const;  
```  
  
#### Parameters  
 [in] `id`  
 A tab ID.  
  
## Return Value  
 The zero-based index of a tab if it is found; -1 if the tab ID is not found.  
  
## Remarks  
 The tab IDs are assigned automatically when tabs are added to a tab control.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)