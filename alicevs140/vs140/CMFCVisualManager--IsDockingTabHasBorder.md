---
title: "CMFCVisualManager::IsDockingTabHasBorder"
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
ms.assetid: 0b0150ec-09db-47f8-9f92-46cdace41d04
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::IsDockingTabHasBorder
Returns whether the current visual manager draws borders around panes that are docked and tabbed.  
  
## Syntax  
  
```  
virtual BOOL IsDockingTabHasBorder();  
```  
  
## Return Value  
 `TRUE` if the visual manager draws borders around panes that are docked and tabbed; `FALSE` otherwise.  
  
## Remarks  
 Docked panes become tabbed when multiple panes are docked to the same location.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)