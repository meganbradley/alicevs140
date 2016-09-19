---
title: "CPaneFrameWnd::OnPaneRecalcLayout"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 51331d5b-1432-4975-bb66-fe3de82adfc1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::OnPaneRecalcLayout
Adjusts the layout of a pane inside a mini-frame window.  
  
## Syntax  
  
```  
virtual void OnPaneRecalcLayout();  
```  
  
## Remarks  
 The framework calls this method when it must adjust the layout of a pane inside the mini-frame window.  
  
 By default, the pane is positioned to cover the complete client area of the mini-frame window.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)