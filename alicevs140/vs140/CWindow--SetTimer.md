---
title: "CWindow::SetTimer"
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
ms.assetid: 9af43e75-d680-4fb6-892b-8dbd90eb0f10
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetTimer
Creates a timer event.  
  
## Syntax  
  
```  
  
      UINT SetTimer(  
   UINT nIDEvent,  
   UINT nElapse,  
   void ( CALLBACK* lpfnTimer )(HWND, UINT, UINT, DWORD) = NULL   
) throw();  
```  
  
## Remarks  
 See [SetTimer](http://msdn.microsoft.com/library/windows/desktop/ms644906) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::KillTimer](../vs140/CWindow--KillTimer.md)