---
title: "CMFCOutlookBarTabCtrl::SetActiveTab"
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
ms.assetid: 6d03fd76-8c0b-425d-9042-f2edf07ae88a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::SetActiveTab
Sets the active tab. The active tab is the one that is open, with its contents visible.  
  
## Syntax  
  
```  
virtual BOOL SetActiveTab(  
   int iTab   
);  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of a tab to be opened.  
  
## Return Value  
 Nonzero if the specified tab has been opened successfully; otherwise 0.  
  
## Remarks  
 The visual effect of setting the active tab depends on whether you have enabled animation. For more information, see [CMFCOutlookBarTabCtrl::EnableAnimation](../vs140/CMFCOutlookBarTabCtrl--EnableAnimation.md).  
  
## Requirements  
 **Header:** afxOutlookBarTabCtrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)