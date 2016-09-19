---
title: "COleControl::InvalidateControl"
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
ms.assetid: d89ca7ce-d71c-476a-99ab-f8c8c1bc4a3d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::InvalidateControl
Forces the control to redraw itself.  
  
## Syntax  
  
```  
  
      void InvalidateControl(   
   LPCRECT lpRect = NULL,   
   BOOL bErase = TRUE    
);  
```  
  
#### Parameters  
 `lpRect`  
 A pointer to the region of the control to be invalidated.  
  
 `bErase`  
 Specifies whether the background within the update region is to be erased when the update region is processed.  
  
## Remarks  
 If `lpRect` has a **NULL** value, the entire control will be redrawn. If `lpRect` is not **NULL**, this indicates the portion of the control's rectangle that is to be invalidated. In cases where the control has no window, or is currently not active, the rectangle is ignored, and a call is made to the client site's [IAdviseSink::OnViewChange](http://msdn.microsoft.com/library/windows/desktop/ms694337) member function. Use this function instead of `CWnd::InvalidateRect` or `InvalidateRect`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::Refresh](../vs140/COleControl--Refresh.md)