---
title: "CWindow::DeferWindowPos"
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
ms.assetid: 051193f2-5777-43d0-a84a-a206cd0f602c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::DeferWindowPos
Updates the specified multiple-window-position structure for the specified window.  
  
## Syntax  
  
```  
  
      HDWP DeferWindowPos(  
   HDWP hWinPosInfo,  
   HWND hWndInsertAfter,  
   int x,  
   int y,  
   int cx,  
   int cy,  
   UINT uFlags   
) throw();  
```  
  
## Remarks  
 See [DeferWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms632681) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)