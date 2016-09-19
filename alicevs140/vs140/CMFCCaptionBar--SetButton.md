---
title: "CMFCCaptionBar::SetButton"
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
ms.assetid: f3c298ba-4cdc-493f-ab4b-e525144f4f94
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::SetButton
Sets the button for the caption bar.  
  
## Syntax  
  
```  
void SetButton(  
   LPCTSTR lpszLabel,  
   UINT uiCmdUI,  
   BarElementAlignment btnAlignmnet=ALIGN_LEFT,  
   BOOL bHasDropDownArrow=TRUE   
);  
```  
  
#### Parameters  
 `lpszLabel`  
 The button's command label.  
  
 `uiCmdUI`  
 The button's command ID.  
  
 `btnAlignmnet`  
 The button's alignment.  
  
 `bHasDropDownArrow`  
 `TRUE` if the button displays a drop down arrow, `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)