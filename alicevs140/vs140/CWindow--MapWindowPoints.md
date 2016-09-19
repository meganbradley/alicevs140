---
title: "CWindow::MapWindowPoints"
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
ms.assetid: 53a50e54-208e-428b-9cda-82dd4b4a9a61
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::MapWindowPoints
Converts a set of points from the window's coordinate space to the coordinate space of another window.  
  
## Syntax  
  
```  
  
      int MapWindowPoints(  
   HWND hWndTo,  
   LPPOINT lpPoint,  
   UINT nCount   
) const throw();  
int MapWindowPoints(  
   HWND hWndTo,  
   LPRECT lpRect   
) const throw();  
```  
  
## Remarks  
 See [MapWindowPoints](http://msdn.microsoft.com/library/windows/desktop/dd145046) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The second version of this method allows you to convert the coordinates of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805)