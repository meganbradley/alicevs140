---
title: "CWnd::SetFont"
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
ms.assetid: fe7308ce-0f51-4f59-9197-f1478295e2ad
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetFont
Sends the `WM_SETFONT` message to the window to use the specified font.  
  
## Syntax  
  
```  
void SetFont(  
   CFont* pFont,  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `pFont`  
 Pointer to a `CFont` object.  
  
 `bRedraw`  
 `TRUE` for the window to redraw immediately after it processes the `WM_SETFONT` message; otherwise `FALSE`.  
  
## Remarks  
 This method has no effect unless the window processes the `WM_SETFONT` message. Many MFC classes that derive from `CWnd` process this message because they are attached to a predefined window class that includes a message handler for the `WM_SETFONT` message. To use this method, classes that you derive from `CWnd` must define a method handler for the `WM_SETFONT` message.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetFont](../vs140/CWnd--GetFont.md)   
 [WM_SETFONT](http://msdn.microsoft.com/library/windows/desktop/ms632642)