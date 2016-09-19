---
title: "CWindow::ClientToScreen"
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
ms.assetid: c098bc5b-92ff-4364-a1ab-2d5342dcb177
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ClientToScreen
Converts client coordinates to screen coordinates.  
  
## Syntax  
  
```  
  
      BOOL ClientToScreen(  
   LPPOINT lpPoint   
) const throw();  
BOOL ClientToScreen(  
   LPRECT lpRect   
) const throw();  
```  
  
## Remarks  
 See [ClientToScreen](http://msdn.microsoft.com/library/windows/desktop/dd183434) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The second version of this method allows you to convert the coordinates of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::ScreenToClient](../vs140/CWindow--ScreenToClient.md)   
 [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805)