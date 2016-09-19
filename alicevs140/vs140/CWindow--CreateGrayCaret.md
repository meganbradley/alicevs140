---
title: "CWindow::CreateGrayCaret"
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
ms.assetid: 877adff8-153a-4d82-9f55-26f4d9c283d4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::CreateGrayCaret
Creates a gray rectangle for the system caret.  
  
## Syntax  
  
```  
  
      BOOL CreateGrayCaret(  
   int nWidth,  
   int nHeight   
) throw();  
```  
  
## Remarks  
 See [CreateCaret](http://msdn.microsoft.com/library/windows/desktop/ms648399) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Passes (HBITMAP) 1 for the bitmap handle parameter to the Win32 function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::CreateCaret](../vs140/CWindow--CreateCaret.md)   
 [CWindow::CreateSolidCaret](../vs140/CWindow--CreateSolidCaret.md)