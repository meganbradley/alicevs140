---
title: "CMFCOutlookBar::OnAfterAnimation"
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
ms.assetid: e7e4016c-75d6-417b-a6a6-27ccacbacc79
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::OnAfterAnimation
Called by [CMFCOutlookBarTabCtrl::SetActiveTab](../vs140/CMFCOutlookBarTabCtrl--SetActiveTab.md) after the active tab has been set using animation.  
  
## Syntax  
  
```  
virtual void OnAfterAnimation(  
   int nPage  
);  
```  
  
#### Parameters  
 [in] `nPage`  
 The zero-based index of the tab page that has been made active.  
  
## Remarks  
 The visual effect of setting the active tab depends on whether you have enabled animation. For more information, see [CMFCOutlookBarTabCtrl::EnableAnimation](../vs140/CMFCOutlookBarTabCtrl--EnableAnimation.md).  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)