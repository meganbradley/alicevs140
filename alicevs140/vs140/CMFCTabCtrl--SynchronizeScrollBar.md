---
title: "CMFCTabCtrl::SynchronizeScrollBar"
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
ms.assetid: 6661eeeb-726d-4221-8107-4a8b4171e1e0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::SynchronizeScrollBar
Draws a horizontal scroll bar on a tab control that displays flat tabs.  
  
## Syntax  
  
```  
BOOL SynchronizeScrollBar(  
   SCROLLINFO* pScrollInfo = NULL  
);  
```  
  
#### Parameters  
 [out] `pScrollInfo`  
 Pointer to a [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537) structure or `NULL`. When this method returns, and if this parameter is not `NULL`, the structure contains all the parameters of the scroll bar. The default value is `NULL`.  
  
## Return Value  
 `TRUE` if this method succeeds; otherwise, `FALSE`.  
  
## Remarks  
 This method affects only a tab control that displays flat tabs. The scroll bar influences all the tabs at the same time.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [SCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb787537)   
 [CMFCTabCtrl::ModifyTabStyle](../vs140/CMFCTabCtrl--ModifyTabStyle.md)