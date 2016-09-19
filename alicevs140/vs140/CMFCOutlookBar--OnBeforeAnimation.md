---
title: "CMFCOutlookBar::OnBeforeAnimation"
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
ms.assetid: 0f578952-ee5b-4c36-80dc-09b909c8242b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::OnBeforeAnimation
Called by [CMFCOutlookBarTabCtrl::SetActiveTab](../vs140/CMFCOutlookBarTabCtrl--SetActiveTab.md) before a tab page is set as the active tab using animation.  
  
## Syntax  
  
```  
virtual BOOL OnBeforeAnimation(  
    int nPage  
);  
```  
  
#### Parameters  
 [in] `nPage`  
 The zero-based index of the tab page that is about to be set active.  
  
## Return Value  
 Returns `TRUE` if animation should be used in setting the new active tab, or `FALSE` if animation should be disabled.  
  
## Remarks  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)