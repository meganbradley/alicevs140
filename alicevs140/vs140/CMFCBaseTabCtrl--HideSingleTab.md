---
title: "CMFCBaseTabCtrl::HideSingleTab"
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
ms.assetid: 58ddfba0-9bae-4ce9-851c-de874a1b99ba
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::HideSingleTab
Sets the option to hide the tabs for the tab control when there is one visible tab.  
  
## Syntax  
  
```  
virtual void HideSingleTab(  
   BOOL bHide = TRUE  
);  
```  
  
#### Parameters  
 [in] `bHide`  
 A Boolean that specifies whether to enable hiding single tabs.  
  
## Remarks  
 When your application is configured to hide single tabs, the framework automatically displays tabs when a second tab is added to the tab control.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)