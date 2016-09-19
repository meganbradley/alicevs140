---
title: "CMFCStatusBar::InvalidatePaneContent"
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
ms.assetid: df4fec20-dce0-4f59-8391-10e2bb0fa0d8
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCStatusBar::InvalidatePaneContent
Invalidate the status bar pane and redraw its content.  
  
## Syntax  
  
```  
void InvalidatePaneContent(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of the pane whose content is to be invalidated and redrawn.  
  
## Remarks  
 When the status bar is invalidated, it is marked for redrawing. Windows redraws it when the `UpdateWindow` method sends a `WM_PAINT` message to the `OnPaint` method.  
  
## Requirements  
 **Header:** afxstatusbar.h  
  
## See Also  
 [CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)