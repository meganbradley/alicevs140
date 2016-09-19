---
title: "CMFCBaseTabCtrl::RemoveAllTabs"
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
ms.assetid: f227533f-3b94-4b38-a91a-887ba9939a97
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::RemoveAllTabs
Removes all the tabs from the tab control.  
  
## Syntax  
  
```  
virtual void RemoveAllTabs();  
```  
  
## Remarks  
 If [CMFCBaseTabCtrl::m_bAutoDestroyWindow](../vs140/CMFCBaseTabCtrl--m_bAutoDestroyWindow.md) is `TRUE`, the framework deletes all the [CWnd](../vs140/CWnd-Class.md) objects attached to the removed tabs.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)