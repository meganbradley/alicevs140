---
title: "CWindow::MoveWindow"
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
ms.assetid: b4ddd92f-41fb-49f3-8fcb-76bfa1bdd01f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::MoveWindow
Changes the window's size and position.  
  
## Syntax  
  
```  
  
      BOOL MoveWindow(  
   int x,  
   int y,  
   int nWidth,  
   int nHeight,  
   BOOL bRepaint = TRUE   
) throw();  
BOOL MoveWindow(  
   LPCRECT lpRect,  
   BOOL bRepaint = TRUE   
) throw();  
```  
  
## Remarks  
 For a top-level window object, the x and y parameters are relative to the upper-left corner of the screen. For a child window object, they are relative to the upper-left corner of the parent window's client area.  
  
 The second version of this method uses a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure to determine the window's new position, width, and height.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetWindowPos](../vs140/CWindow--SetWindowPos.md)