---
title: "CPane::IsInFloatingMultiPaneFrameWnd"
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
ms.assetid: 9bd7068c-4130-4fea-a334-18fe975df5b5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::IsInFloatingMultiPaneFrameWnd
Specifies whether the pane is in a multi-pane frame window ([CMultiPaneFrameWnd Class](../vs140/CMultiPaneFrameWnd-Class.md)).  
  
## Syntax  
  
```  
virtual BOOL IsInFloatingMultiPaneFrameWnd() const;  
```  
  
## Return Value  
 `TRUE` if the pane is in a multi-pane frame window; otherwise, `FALSE`.  
  
## Remarks  
 Only dockable panes can float in a multi-pane frame window. Therefore, `CPane::IsInFloatingMultiPaneFrameWnd` always returns `FALSE`.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMultiPaneFrameWnd Class](../vs140/CMultiPaneFrameWnd-Class.md)   
 [CDockablePane::IsInFloatingMultiPaneFrameWnd](../vs140/CDockablePane--IsInFloatingMultiPaneFrameWnd.md)