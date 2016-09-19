---
title: "CWindow::SetHotKey"
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
ms.assetid: 843278ae-e4ef-47c7-9ce4-95604761a7e7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetHotKey
Associates a hot key with the window by sending a **WM_SETHOTKEY** message.  
  
## Syntax  
  
```  
  
      int SetHotKey(  
   WORD wVirtualKeyCode,  
   WORD wModifiers   
) throw();  
```  
  
#### Parameters  
 `wVirtualKeyCode`  
 [in] The virtual key code of the hot key. For a list of of standard virtual key codes, see Winuser.h.  
  
 `wModifiers`  
 [in] The modifiers of the hot key. For a list of possible values, see **WM_SETHOTKEY** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 For a list of possible return values, see [WM_SETHOTKEY](http://msdn.microsoft.com/library/windows/desktop/ms646284) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetHotKey](../vs140/CWindow--GetHotKey.md)