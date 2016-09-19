---
title: "CMFCColorButton::UpdateColor"
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
ms.assetid: d8af72f8-ddef-4957-a5f5-06b7411744e1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::UpdateColor
Called by the framework when the user selects a color from the color bar that displays when the user clicks the color button.  
  
## Syntax  
  
```  
virtual void UpdateColor(  
   COLORREF color   
);  
```  
  
#### Parameters  
 [in] `color`  
 A color selected by the user.  
  
## Remarks  
 The `UpdateColor` function changes the currently selected button's color and notifies its parent by sending a `WM_COMMAND` message with a `BN_CLICKED` standard notification. Use the [GetColor](../vs140/CMFCColorButton--GetColor.md) method to retrieve the selected color.  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)