---
title: "CWindow::ScreenToClient"
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
ms.assetid: 0ab56f1e-7d43-4860-8df0-a963dfc27f5d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ScreenToClient
Converts screen coordinates to client coordinates.  
  
## Syntax  
  
```  
  
      BOOL ScreenToClient(  
   LPPOINT lpPoint   
) const throw();  
BOOL ScreenToClient(  
   LPRECT lpRect   
) const throw();  
```  
  
## Remarks  
 See [ScreenToClient](http://msdn.microsoft.com/library/windows/desktop/dd162952) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The second version of this method allows you to convert the coordinates of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::ClientToScreen](../vs140/CWindow--ClientToScreen.md)   
 [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805)