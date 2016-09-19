---
title: "CMDIFrameWndEx::OnCloseMiniFrame"
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
ms.assetid: 4fed69c3-e733-44d0-89bc-98e5c84870ea
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnCloseMiniFrame
Called by the framework when the user clicks the **Close** button on a floating mini-frame window.  
  
## Syntax  
  
```  
virtual BOOL OnCloseMiniFrame(  
   CPaneFrameWnd*    
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 Pointer to the mini-frame window being closed.  
  
## Return Value  
 `TRUE` if the floating mini-frame window can be closed. Otherwise, `FALSE`.  
  
## Remarks  
 Override this method to handle hiding of floating mini-frame windows. Return `FALSE` if you want to prevent a floating mini-frame window from being hidden.  
  
 The default implementation does nothing and returns `TRUE`.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)