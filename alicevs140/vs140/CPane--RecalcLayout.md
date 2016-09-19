---
title: "CPane::RecalcLayout"
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
ms.assetid: ff0b0804-f58a-45a5-9844-012e3dca50f6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::RecalcLayout
Recalculates layout information for the pane.  
  
## Syntax  
  
```  
virtual void RecalcLayout();  
```  
  
## Remarks  
 If the pane is docked, this method updates the virtual rectangle for the pane by setting its size to the current size of the pane.  
  
 If the pane is floating, this method notifies the parent mini-frame to adjust the size of the pane to the size of the mini-frame. The framework ensures that the mini-frame is at least the minimum allowed size for the pane ([CPane::GetMinSize](../vs140/CPane--GetMinSize.md)) and resizes the mini-frame if necessary.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)