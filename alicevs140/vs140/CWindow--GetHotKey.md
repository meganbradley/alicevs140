---
title: "CWindow::GetHotKey"
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
ms.assetid: a20fb852-d71b-45c2-8511-955c87e9289a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetHotKey
Determines the hot key associated with the window by sending a **WM_GETHOTKEY** message.  
  
## Syntax  
  
```  
  
DWORD GetHotKey( ) const throw();  
  
```  
  
## Return Value  
 The virtual key code and modifiers for the hot key associated with the window. For a list of possible modifiers, see [WM_GETHOTKEY](http://msdn.microsoft.com/library/windows/desktop/ms646278) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For a list of of standard virtual key codes, see Winuser.h.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetHotKey](../vs140/CWindow--SetHotKey.md)