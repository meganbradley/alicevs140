---
title: "CMFCColorMenuButton::EnableTearOff"
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
ms.assetid: b29d317b-3d62-44a8-adab-99858c47355b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::EnableTearOff
Enables the ability to tear off a color pane.  
  
## Syntax  
  
```  
void EnableTearOff(  
   UINT uiID,  
   int nVertDockColumns=-1,  
   int nHorzDockRows=-1   
);  
```  
  
#### Parameters  
 [in] `uiID`  
 Specifies the ID for the tear-off pane.  
  
 [in] `nVertDockColumns`  
 Specifies the number of columns in the vertically docked color pane while in tear-off state.  
  
 [in] `nHorzDockRows`  
 Specifies the number of rows for the horizontally docked color pane while in tear-off state.  
  
## Remarks  
 Call this method to enable the "tear-off" feature for the color pane that pops up when the `CMFCColorMenuButton` button is pressed.  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)