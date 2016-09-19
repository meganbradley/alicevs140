---
title: "CMFCOutlookBarTabCtrl::EnableScrollButtons"
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
ms.assetid: 225ed801-28c2-46b7-98e5-51a3cfb9810d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarTabCtrl::EnableScrollButtons
Called by the framework to enable scroll handles that allow the user to scroll through buttons on the Outlook bar pane.  
  
## Syntax  
  
```  
void EnableScrollButtons(  
   BOOL bEnable = TRUE,  
   BOOL bIsUp = TRUE,  
   BOOL bIsDown = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 Determines whether the scroll buttons are displayed.  
  
 [in] `bIsUp`  
 Determines whether the top scrollbar is displayed.  
  
 [in] `bIsDown`  
 Determines whether the bottom scrollbar is displayed.  
  
## Remarks  
 Enables the display of the scroll buttons. This method is called by the framework when the active tab changes to restore the scroll buttons.  
  
## Requirements  
 **Header:** afxoutlookbartabctrl.h  
  
## See Also  
 [CMFCOutlookBarTabCtrl Class](../vs140/CMFCOutlookBarTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)