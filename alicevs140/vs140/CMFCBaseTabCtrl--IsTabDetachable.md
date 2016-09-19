---
title: "CMFCBaseTabCtrl::IsTabDetachable"
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
ms.assetid: 390cd6b1-2eaa-427f-8ad8-ff15f8670bb4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::IsTabDetachable
Determines whether a tab is detachable.  
  
## Syntax  
  
```  
virtual BOOL IsTabDetachable(  
   int iTab  
) const;  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab to check.  
  
## Return Value  
 `TRUE` if the tab is detachable; `FALSE` otherwise.  
  
## Remarks  
 To make a tab detachable, use the method [CMFCBaseTabCtrl::EnableTabDetach](../vs140/CMFCBaseTabCtrl--EnableTabDetach.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::EnableTabDetach](../vs140/CMFCBaseTabCtrl--EnableTabDetach.md)