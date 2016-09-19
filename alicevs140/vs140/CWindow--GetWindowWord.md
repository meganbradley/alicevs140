---
title: "CWindow::GetWindowWord"
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
ms.assetid: 6e92436a-49b7-4506-97f8-6fbf8874e94d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetWindowWord
Retrieves a 16-bit value at a specified offset into the extra window memory.  
  
## Syntax  
  
```  
  
      WORD GetWindowWord(  
   int nIndex   
) const throw();  
```  
  
## Remarks  
 See [GetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633584) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetWindowWord](../vs140/CWindow--SetWindowWord.md)   
 [CWindow::GetWindowLong](../vs140/CWindow--GetWindowLong.md)