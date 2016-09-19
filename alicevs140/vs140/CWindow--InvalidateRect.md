---
title: "CWindow::InvalidateRect"
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
ms.assetid: 3fad996b-1673-474e-a678-d70423344186
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::InvalidateRect
Invalidates the client area within the specified rectangle.  
  
## Syntax  
  
```  
  
      BOOL InvalidateRect(  
   LPCRECT lpRect,  
   BOOL bErase = TRUE   
) throw();  
```  
  
## Remarks  
 See [InvalidateRect](http://msdn.microsoft.com/library/windows/desktop/dd145002) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::Invalidate](../vs140/CWindow--Invalidate.md)   
 [CWindow::InvalidateRgn](../vs140/CWindow--InvalidateRgn.md)   
 [CWindow::ValidateRect](../vs140/CWindow--ValidateRect.md)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)