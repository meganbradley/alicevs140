---
title: "CMFCOutlookBarTabCtrl::CanShowMorePageButtons"
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
ms.assetid: 6077d00d-c642-4ead-a6eb-f75669ad2d37
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::CanShowMorePageButtons
Called by the framework during resizing operations to determine whether more Outlook bar tab page buttons can be displayed than are currently visible.  
  
## Syntax  
  
```  
virtual BOOL CanShowMorePageButtons() const;  
```  
  
## Return Value  
 `TRUE` if there are buttons that are not currently visible; otherwise `FALSE`.  
  
## Remarks  
 The Outlook bar tab control dynamically adds or removes tabs from the display, depending on how much room is available. This method is used by the framework to assist in that process.  
  
## Requirements  
 **Header:** afxoutlookbartabctrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)