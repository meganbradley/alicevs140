---
title: "CWindow::GetTopLevelWindow"
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
ms.assetid: 0e3398a8-d1ef-4996-9eb7-5fae7e0355e0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetTopLevelWindow
Retrieves the window's top-level parent or owner window.  
  
## Syntax  
  
```  
  
HWND GetTopLevelWindow( ) const throw();  
  
```  
  
## Return Value  
 The handle to the top-level owner window.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetTopLevelParent](../vs140/CWindow--GetTopLevelParent.md)   
 [CWindow::GetWindow](../vs140/CWindow--GetWindow.md)