---
title: "CWindow::SetWindowWord"
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
ms.assetid: c53fd093-6800-419e-8a98-46968fc2486f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetWindowWord
Sets a 16-bit value at a specified offset into the extra window memory.  
  
## Syntax  
  
```  
  
      WORD SetWindowWord(  
   int nIndex,  
   WORD wNewWord   
) throw();  
```  
  
## Remarks  
 See [SetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633591) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowWord](../vs140/CWindow--GetWindowWord.md)   
 [CWindow::SetWindowLong](../vs140/CWindow--SetWindowLong.md)