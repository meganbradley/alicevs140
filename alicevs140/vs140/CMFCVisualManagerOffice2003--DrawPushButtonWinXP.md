---
title: "CMFCVisualManagerOffice2003::DrawPushButtonWinXP"
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
ms.assetid: b41c90d6-4791-45f3-9b6a-c4ffd7b9ac9a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::DrawPushButtonWinXP
Draws a push button using the current Windows XP theme.  
  
## Syntax  
  
```  
virtual BOOL DrawPushButtonWinXP(  
   CDC* pDC,  
   CRect rect,  
   CMFCButton* pButton,  
   UINT uiState  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 The bounding rectangle of the push button.  
  
 [in] `pButton`  
 A pointer to the [CMFCButton Class](../vs140/CMFCButton-Class.md) object to draw.  
  
 [in] `uiState`  
 Ignored. The state is taken from `pButton`.  
  
## Return Value  
 `TRUE` if the Theme API is enabled; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)