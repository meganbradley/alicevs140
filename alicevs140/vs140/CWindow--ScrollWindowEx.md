---
title: "CWindow::ScrollWindowEx"
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
ms.assetid: e9f92cb5-a2bc-466d-a3c7-ba1f176fc0b8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ScrollWindowEx
Scrolls the specified client area with additional features.  
  
## Syntax  
  
```  
  
      int ScrollWindowEx(  
   int dx,  
   int dy,  
   LPCRECT lpRectScroll,  
   LPCRECT lpRectClip,  
   HRGN hRgnUpdate,  
   LPRECT lpRectUpdate,  
   UINT flags   
) throw();  
```  
  
## Remarks  
 See [ScrollWindowEx](http://msdn.microsoft.com/library/windows/desktop/bb787593) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::ScrollWindow](../vs140/CWindow--ScrollWindow.md)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)