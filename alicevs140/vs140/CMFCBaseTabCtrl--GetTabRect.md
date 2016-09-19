---
title: "CMFCBaseTabCtrl::GetTabRect"
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
ms.assetid: 412d4e52-dbbf-4b8a-8174-6fb98e377af6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabRect
Retrieves the size and position of the specified tab.  
  
## Syntax  
  
```  
virtual BOOL GetTabRect(  
   int iTab,  
   CRect& rect  
) const;  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab.  
  
 [out] `rect`  
 A reference to a `CRect` object. This method stores the size and position of the tab in this parameter.  
  
## Return Value  
 `TRUE` if successful; `FALSE` if the tab index is invalid.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)