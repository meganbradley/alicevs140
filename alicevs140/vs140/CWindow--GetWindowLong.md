---
title: "CWindow::GetWindowLong"
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
ms.assetid: 08e6417d-f901-48c3-83b4-66f634f58341
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetWindowLong
Retrieves a 32-bit value at a specified offset into the extra window memory.  
  
## Syntax  
  
```  
  
      LONG GetWindowLong(  
   int nIndex   
) const throw();  
```  
  
## Remarks  
 See [GetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633584) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
> [!NOTE]
>  To write code that is compatible with both 32-bit and 64-bit versions of Windows, use [CWindow::GetWindowLongPtr](../vs140/CWindow--GetWindowLongPtr.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetWindowLong](../vs140/CWindow--SetWindowLong.md)   
 [CWindow::GetWindowWord](../vs140/CWindow--GetWindowWord.md)