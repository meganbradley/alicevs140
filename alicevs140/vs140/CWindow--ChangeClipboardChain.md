---
title: "CWindow::ChangeClipboardChain"
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
ms.assetid: 0f3e8b9e-b0c9-4585-8b20-e3818a5cdd6f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ChangeClipboardChain
Removes the window from the chain of Clipboard viewers.  
  
## Syntax  
  
```  
  
      BOOL ChangeClipboardChain(  
   HWND hWndNewNext   
) throw();  
```  
  
## Remarks  
 See [ChangeClipboardChain](http://msdn.microsoft.com/library/windows/desktop/ms649034) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetClipboardViewer](../vs140/CWindow--SetClipboardViewer.md)