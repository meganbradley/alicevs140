---
title: "CPane::GetAvailableStretchSize"
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
ms.assetid: 54dd9997-ea29-44bb-90e4-092f276dd1fa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::GetAvailableStretchSize
Returns the amount, in pixels, that the pane can shrink.  
  
## Syntax  
  
```  
virtual int GetAvailableStretchSize() const;  
```  
  
## Return Value  
 The amount, in pixels, that the pane can shrink. If the pane is docked horizontally, this amount is the available width; otherwise, it is the available height.  
  
## Remarks  
 The available stretch size is calculated by subtracting the minimum allowed size for the pane ([CPane::GetMinSize](../vs140/CPane--GetMinSize.md)) from the current size ([CWnd::GetWindowRect](../vs140/CWnd--GetWindowRect.md)).  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)