---
title: "CMFCRibbonBar::SetWindows7Look"
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
ms.assetid: d922ae52-5aa5-4482-9035-ee57ae6f876d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::SetWindows7Look
Enables or disables Windows 7 look (small rectangular application button) for the Ribbon.  
  
## Syntax  
  
```  
void SetWindows7Look(  
   BOOL bWindows7Look,  
   BOOL bRecalc = TRUE  
);  
```  
  
#### Parameters  
 `bWindows7Look`  
 `TRUE` sets Windows 7 look; `FALSE` otherwise.  
  
 `bRecalc`  
 `TRUE` recalculates the ribbon layout; `FALSE` otherwise.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)