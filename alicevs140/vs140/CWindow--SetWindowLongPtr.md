---
title: "CWindow::SetWindowLongPtr"
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
ms.assetid: 322267a7-63d4-4803-b6be-0719cef89cf9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetWindowLongPtr
Changes an attribute of the specified window, and also sets a value at the specified offset in the extra window memory.  
  
## Syntax  
  
```  
  
      LONG_PTR SetWindowLongPtr(  
   int nIndex,  
   LONG_PTR dwNewLong   
) throw( );  
```  
  
## Remarks  
 See [SetWindowLongPtr](http://msdn.microsoft.com/library/windows/desktop/ms644898) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 This function supersedes the `CWindow::SetWindowLong` method. To write code that is compatible with both 32-bit and 64-bit versions of Windows, use `CWindow::SetWindowLongPtr`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowLongPtr](../vs140/CWindow--GetWindowLongPtr.md)   
 [CWindow::SetWindowLong](../vs140/CWindow--SetWindowLong.md)