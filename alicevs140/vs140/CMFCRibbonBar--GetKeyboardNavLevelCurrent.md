---
title: "CMFCRibbonBar::GetKeyboardNavLevelCurrent"
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
ms.assetid: aafe0958-7a99-4394-95cf-547cb166ce5f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetKeyboardNavLevelCurrent
Retrieves the current keyboard navigation object on the ribbon bar.  
  
## Syntax  
  
```  
CObject* GetKeyboardNavLevelCurrent() const;  
```  
  
## Return Value  
 The current keyboard navigation object on the ribbon bar; otherwise `NULL` if no object currently displays keytips.  
  
## Remarks  
 The object that is currently displaying keytips is the current keyboard navigation object.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)