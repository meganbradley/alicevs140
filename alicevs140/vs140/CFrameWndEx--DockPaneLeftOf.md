---
title: "CFrameWndEx::DockPaneLeftOf"
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
ms.assetid: 92d9b686-e325-47e1-8bd8-fc66360cd99d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::DockPaneLeftOf
Docks the specified pane to the left of another pane.  
  
## Syntax  
  
```  
BOOL DockPaneLeftOf(  
   CPane* pBar,  
   CPane* pLeftOf   
);  
```  
  
#### Parameters  
 [in] `pBar`  
 A pointer to the pane object to be docked.  
  
 [in] `pLeftOf`  
 A pointer to the pane to the left of which to dock the pane specified by `pBar`.  
  
## Return Value  
 `TRUE` if `pBar` is docked successfully. `FALSE` otherwise.  
  
## Remarks  
 The method takes the toolbar specified by the `pBar` parameter and docks it at the left side of the toolbar specified by `pLeftOf` parameter.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)