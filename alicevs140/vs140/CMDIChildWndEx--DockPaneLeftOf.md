---
title: "CMDIChildWndEx::DockPaneLeftOf"
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
ms.assetid: fbb23334-a8dd-41f9-a043-2b105177f8c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::DockPaneLeftOf
Docks one pane to the left of another pane.  
  
## Syntax  
  
```  
BOOL DockPaneLeftOf(  
   CPane* pBar,  
   CPane* pLeftOf   
);  
```  
  
#### Parameters  
 `pBar`  
 A pointer to the pane that is to be docked.  
  
 `pLeftOf`  
 A pointer to the pane that serves as the point of reference.  
  
## Return Value  
 `TRUE` on success, `FALSE` on failure.  
  
## Remarks  
 This method takes the pane specified by `pBar` and docks it at the left side of the pane specified by `pLeftOf`.  
  
 Call this method when you want to dock several panes in predefined order.  
  
## Requirements  
 **Header:** afxMDIChildWndEx.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)