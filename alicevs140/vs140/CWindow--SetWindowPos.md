---
title: "CWindow::SetWindowPos"
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
ms.assetid: bb344ced-f6b9-4f5a-91a6-9b874a16fe60
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetWindowPos
Sets the size, position, and Z order.  
  
## Syntax  
  
```  
  
      BOOL SetWindowPos(  
   HWND hWndInsertAfter,  
   int x,  
   int y,  
   int cx,  
   int cy,  
   UINT nFlags   
) throw();  
BOOL SetWindowPos(  
   HWND hWndInsertAfter,  
   LPCRECT lpRect,  
   UINT nFlags   
) throw();  
```  
  
## Remarks  
 See [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The second version of this method uses a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure to set the window's new position, width, and height.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::BringWindowToTop](../vs140/CWindow--BringWindowToTop.md)   
 [CWindow::MoveWindow](../vs140/CWindow--MoveWindow.md)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)