---
title: "CMFCRibbonBar::GetHideFlags"
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
ms.assetid: 070e9561-6ed6-4f99-a96d-64c5bbe659b2
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetHideFlags
Retrieves the flags that indicate how much of the ribbon bar is visible.  
  
## Syntax  
  
```  
DWORD GetHideFlags() const;  
```  
  
## Return Value  
 The flags that indicate how much of the ribbon bar is visible.  
  
## Remarks  
 The following table lists the possible combination of flags for the return value:  
  
 `AFX_RIBBONBAR_HIDE_ELEMENTS`  
 The ribbon bar is minimized vertically and only the category tabs, main button, and quick access toolbar are visible.  
  
 `AFX_RIBBONBAR_HIDE_ALL`  
 The width of the ribbon bar is less than the minimum width and is completely hidden.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)