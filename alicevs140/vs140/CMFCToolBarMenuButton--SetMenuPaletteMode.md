---
title: "CMFCToolBarMenuButton::SetMenuPaletteMode"
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
ms.assetid: 537c7ffa-2691-4536-91ca-d2ae1c3f38ee
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::SetMenuPaletteMode
Specifies whether the drop-down menu is in palette mode.  
  
## Syntax  
  
```  
void SetMenuPaletteMode(  
   BOOL bMenuPaletteMode=TRUE,  
   int nPaletteRows=1   
);  
```  
  
#### Parameters  
 [in] `bMenuPaletteMode`  
 Specifies whether the drop-down menu is in palette mode.  
  
 [in] `nPaletteRows`  
 Number of rows in palette.  
  
## Remarks  
 In the palette mode, all menu items are displayed as a multicolumn palette. You specify the number of rows by using `nPaletteRows`.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)