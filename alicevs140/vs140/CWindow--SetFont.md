---
title: "CWindow::SetFont"
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
ms.assetid: 998c351b-80bd-4d22-b5cd-80f72c0fc1f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetFont
Changes the window's current font by sending a [WM_SETFONT](http://msdn.microsoft.com/library/windows/desktop/ms632642) message to the window.  
  
## Syntax  
  
```  
  
      void SetFont(  
   HFONT hFont,  
   BOOL bRedraw = TRUE   
) throw();  
```  
  
#### Parameters  
 `hFont`  
 [in] The handle to the new font.  
  
 `bRedraw`  
 [in] If **TRUE** (the default value), the window is redrawn. Otherwise, it is not.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetFont](../vs140/CWindow--GetFont.md)