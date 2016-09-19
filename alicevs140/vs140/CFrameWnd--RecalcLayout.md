---
title: "CFrameWnd::RecalcLayout"
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
ms.assetid: a04f3354-a6fb-4b33-998f-b92946081a04
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::RecalcLayout
Called by the framework when the standard control bars are toggled on or off or when the frame window is resized.  
  
## Syntax  
  
```  
  
      virtual void RecalcLayout(  
   BOOL bNotify = TRUE   
);  
```  
  
#### Parameters  
 `bNotify`  
 Determines whether the active in-place item for the frame window receives notification of the layout change. If **TRUE**, the item is notified; otherwise **FALSE**.  
  
## Remarks  
 The default implementation of this member function calls the `CWnd` member function `RepositionBars` to reposition all the control bars in the frame as well as in the main client window (usually a `CView` or **MDICLIENT**).  
  
 Override this member function to control the appearance and behavior of control bars after the layout of the frame window has changed. For example, call it when you turn control bars on or off or add another control bar.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::RepositionBars](../vs140/CWnd--RepositionBars.md)