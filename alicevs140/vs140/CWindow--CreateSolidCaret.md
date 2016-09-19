---
title: "CWindow::CreateSolidCaret"
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
ms.assetid: b52695fe-6187-4d38-911c-591e34cc7a8a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::CreateSolidCaret
Creates a solid rectangle for the system caret.  
  
## Syntax  
  
```  
  
      BOOL CreateSolidCaret(  
   int nWidth,  
   int nHeight   
) throw();  
```  
  
## Remarks  
 See [CreateCaret](http://msdn.microsoft.com/library/windows/desktop/ms648399) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Passes (HBITMAP) 0 for the bitmap handle parameter to the Win32 function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::CreateCaret](../vs140/CWindow--CreateCaret.md)   
 [CWindow::CreateGrayCaret](../vs140/CWindow--CreateGrayCaret.md)