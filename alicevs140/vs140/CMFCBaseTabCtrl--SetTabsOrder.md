---
title: "CMFCBaseTabCtrl::SetTabsOrder"
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
ms.assetid: 406d49c7-d043-4a56-80f7-e88e425d5a85
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetTabsOrder
Arranges the tabs in the specified order.  
  
## Syntax  
  
```  
BOOL SetTabsOrder(  
   const CArray<int,int>& arOrder   
);  
```  
  
#### Parameters  
 [in] `arOrder`  
 An array of zero-based indexes that defines the new tab order.  
  
## Return Value  
 `TRUE` if successful; `FAIL` otherwise.  
  
## Remarks  
 The size of the `arOrder` array must be equal to the number of tabs in the tab control.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)