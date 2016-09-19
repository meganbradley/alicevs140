---
title: "CMFCBaseVisualManager::DrawPushButton"
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
ms.assetid: 1f90a3dc-0330-42f2-8170-11867794f8cd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseVisualManager::DrawPushButton
Draws a push button using the current Windows theme.  
  
## Syntax  
  
```  
virtual BOOL DrawPushButton(  
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
 `TRUE` if Theme API is enabled; otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCBaseVisualManager Class](../vs140/CMFCBaseVisualManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)