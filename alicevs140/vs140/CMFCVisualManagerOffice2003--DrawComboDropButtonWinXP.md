---
title: "CMFCVisualManagerOffice2003::DrawComboDropButtonWinXP"
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
ms.assetid: 193ba67d-fd66-47af-af42-b763e9224164
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::DrawComboDropButtonWinXP
Draws a combo box drop-down button using the current Windows XP theme.  
  
## Syntax  
  
```  
virtual BOOL DrawComboDropButtonWinXP(  
   CDC* pDC,  
   CRect rect,  
   BOOL bDisabled,  
   BOOL bIsDropped,  
   BOOL bIsHighlighted  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 The bounding rectangle of the combo box drop-down button.  
  
 [in] `bDisabled`  
 Specifies whether the combo box drop-down button is disabled.  
  
 [in] `bIsDropped`  
 Specifies whether the combo box drop-down button is dropped down.  
  
 [in] `bIsHighlighted`  
 Specifies whether the combo box drop-down button is highlighted.  
  
## Return Value  
 Returns `TRUE` if the theme API is enabled or `FALSE` if not.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)