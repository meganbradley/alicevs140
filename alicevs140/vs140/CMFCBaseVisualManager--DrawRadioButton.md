---
title: "CMFCBaseVisualManager::DrawRadioButton"
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
ms.assetid: aad54f21-7589-4148-97bb-0788256c2856
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseVisualManager::DrawRadioButton
Draws a radio button control by using the current Windows theme.  
  
## Syntax  
  
```  
virtual BOOL DrawRadioButton(  
   CDC *pDC,   
   CRect rect,   
   BOOL bHighlighted,   
   BOOL bChecked,   
   BOOL bEnabled,   
   BOOL bPressed    
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 The bounding rectangle of the radio button.  
  
 [in] `bHighlighted`  
 Specifies whether the radio button is highlighted.  
  
 [in] `bChecked`  
 Specifies whether the radio button is checked.  
  
 [in] `bEnabled`  
 Specifies whether the radio button is enabled.  
  
 [in] `bPressed`  
 Specifies whether the radio button is pressed.  
  
## Return Value  
 `TRUE` if Theme API is enabled; otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCBaseVisualManager Class](../vs140/CMFCBaseVisualManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)