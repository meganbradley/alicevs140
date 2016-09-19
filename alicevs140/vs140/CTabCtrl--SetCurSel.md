---
title: "CTabCtrl::SetCurSel"
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
ms.assetid: c77d2468-0801-444d-8286-2710b3c32c94
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::SetCurSel
Selects a tab in a tab control.  
  
## Syntax  
  
```  
  
      int SetCurSel(  
  int nItem   
);  
```  
  
#### Parameters  
 `nItem`  
 The zero-based index of the item to be selected.  
  
## Return Value  
 Zero-based index of the previously selected tab if successful, otherwise – 1.  
  
## Remarks  
 A tab control does not send a **TCN_SELCHANGING** or **TCN_SELCHANGE** notification message when a tab is selected using this function. These notifications are sent, using **WM_NOTIFY**, when the user clicks or uses the keyboard to change tabs.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::GetCurSel](../vs140/CTabCtrl--GetCurSel.md)   
 [CTabCtrl::GetCurFocus](../vs140/CTabCtrl--GetCurFocus.md)