---
title: "CMFCBaseTabCtrl::EnableTabDetach"
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
ms.assetid: 8909e922-2dbe-4e18-9d24-acba16e99673
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::EnableTabDetach
Enables detachable tabs.  
  
## Syntax  
  
```  
virtual BOOL EnableTabDetach(  
   int iTab,  
   BOOL bEnable  
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of a tab.  
  
 [in] `bEnable`  
 A Boolean that indicates whether to make the tab detachable.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)