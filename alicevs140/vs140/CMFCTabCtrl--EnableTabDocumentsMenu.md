---
title: "CMFCTabCtrl::EnableTabDocumentsMenu"
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
ms.assetid: 892da643-42c6-4b95-bb29-dab139e18f22
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::EnableTabDocumentsMenu
Toggles between a user interface that uses two buttons to scroll the window tabs and an interface that displays a pop-up menu of tabbed windows.  
  
## Syntax  
  
```  
void EnableTabDocumentsMenu(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to display a pop-up menu of tabbed window labels; `FALSE` to display forward and backward scroll buttons. The default value is `TRUE`.  
  
## Remarks  
 When the user clicks a tab label, the framework displays the corresponding tabbed window. If the tab label is visible, the tabbed window is opened without changing its position. If the user selects a document from the pop-up menu and the corresponding tabbed window is off screen, the tabbed window becomes the first tab.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)