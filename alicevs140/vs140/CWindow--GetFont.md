---
title: "CWindow::GetFont"
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
ms.assetid: c45e0578-a7b2-4c09-9448-ef0435dddfca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetFont
Retrieves the window's current font by sending a [WM_GETFONT](http://msdn.microsoft.com/library/windows/desktop/ms632624) message to the window.  
  
## Syntax  
  
```  
  
HFONT GetFont( ) const throw();  
```  
  
## Return Value  
 A font handle.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetFont](../vs140/CWindow--SetFont.md)