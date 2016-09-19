---
title: "CMDIFrameWndEx::OnDrawMenuLogo"
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
ms.assetid: 2022ec3f-3a8f-41ac-9555-1cd55ac8ca72
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnDrawMenuLogo
Called by the framework when a [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md)processes a `WM_PAINT` message.  
  
## Syntax  
  
```  
virtual void OnDrawMenuLogo(  
   CDC* ,  
   CMFCPopupMenu* ,  
   const CRect&    
);  
```  
  
## Remarks  
 Override this function to display a logo on the pop-up menu that belongs to the menu bar owned by the `CMDIFrameWndEx`-derived object. The default implementation does nothing.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)