---
title: "CBasePane::IsVisible"
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
ms.assetid: f5869acd-ff6e-43f2-9842-b0afb4255ddd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsVisible
Determines whether the pane is visible.  
  
## Syntax  
  
```  
virtual BOOL IsVisible() const;  
```  
  
## Return Value  
 `TRUE` if the pane is visible; otherwise `FALSE`.  
  
## Remarks  
 Use this method to determine the visibility of a pane. Do not use `::IsWindowVisible`.  
  
 If the pane is not tabbed (see [CBasePane::IsTabbed](../vs140/CBasePane--IsTabbed.md)), this method checks for the `WS_VISIBLE` style. If the pane is tabbed, this method checks the visibility of the parent tabbed window. If the parent window is visible, the function checks the visibility of the pane tab using [CMFCBaseTabCtrl::IsTabVisible](../vs140/CMFCBaseTabCtrl--IsTabVisible.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)