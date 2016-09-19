---
title: "CMFCBaseTabCtrl::SetTabBkColor"
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
ms.assetid: 8aff5d52-5722-407a-bec7-c9863c51a692
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetTabBkColor
Sets the background color for the specified tab.  
  
## Syntax  
  
```  
virtual BOOL SetTabBkColor(  
   int iTab,  
   COLORREF color = (COLORREF)-1  
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab.  
  
 [in] `color`  
 The color to set.  
  
## Return Value  
 `TRUE` if successful; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)