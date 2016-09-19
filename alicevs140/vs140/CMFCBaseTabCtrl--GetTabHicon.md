---
title: "CMFCBaseTabCtrl::GetTabHicon"
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
ms.assetid: d915b667-1041-4f57-afac-0419671ee418
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabHicon
Returns the HICON associated with the specified tab.  
  
## Syntax  
  
```  
virtual HICON GetTabHicon(  
   int iTab  
) const;  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index for the tab.  
  
## Return Value  
 The HICON associated with a tab label if successful; `NULL` if there is no HICON or if the method fails.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::SetTabHicon](../vs140/CMFCBaseTabCtrl--SetTabHicon.md)