---
title: "CMDIFrameWndEx::RecalcLayout"
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
ms.assetid: 08929d06-9d1c-4b27-8b69-7cc179d256dc
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::RecalcLayout
Called by the framework to recalculate the layout of the frame window.  
  
## Syntax  
  
```  
virtual void RecalcLayout(  
   BOOL bNotify = TRUE  
);  
```  
  
#### Parameters  
 [in] `bNotify`  
 Determines whether the active in-place item for the frame window receives notification of the layout change. If `TRUE`, the item is notified; otherwise `FALSE`.  
  
## Remarks  
 This method overrides [CFrameWnd::RecalcLayout](../vs140/CFrameWnd--RecalcLayout.md).  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)