---
title: "CMDIFrameWndEx::AdjustDockingLayout"
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
ms.assetid: adeea31e-cb66-493a-948c-61433e14d431
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::AdjustDockingLayout
Recalculates the layout of all docked panes.  
  
## Syntax  
  
```  
virtual void AdjustDockingLayout(  
   HDWP hdwp=NULL   
);  
```  
  
#### Parameters  
 [in] `hdwp`  
 Identifies the multiple-window-position structure. You can obtain this value by calling `BeginDeferWindowPos`.  
  
## Remarks  
 Call this member function to recalculate the layout of all panes docked to the frame window.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)