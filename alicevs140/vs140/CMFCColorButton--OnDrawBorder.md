---
title: "CMFCColorButton::OnDrawBorder"
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
ms.assetid: 37036a42-8589-4076-8d3f-1a53d476fb10
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::OnDrawBorder
Called by the framework to display the border of the button.  
  
## Syntax  
  
```  
virtual void OnDrawBorder(  
   CDC* pDC,  
   CRect& rectClient,  
   UINT uiState   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Points to the device context used to draw the border.  
  
 [in] `rectClient`  
 A rectangle in the device context that is specified by the the `pDC` parameter that defines the boundaries of the button to be drawn.  
  
 [in] `uiState`  
 Specifies the visual state of the button.  
  
## Remarks  
 Override this function to customize the color button's border appearance.  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)