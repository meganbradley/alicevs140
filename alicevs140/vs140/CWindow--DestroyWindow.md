---
title: "CWindow::DestroyWindow"
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
ms.assetid: 070fcb24-ebce-4f51-9335-26665dfdbd82
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::DestroyWindow
Destroys the window associated with the `CWindow` object and sets [m_hWnd](../vs140/CWindow--m_hWnd.md) to **NULL**.  
  
## Syntax  
  
```  
  
BOOL DestroyWindow( ) throw();  
```  
  
## Remarks  
 See [DestroyWindow](http://msdn.microsoft.com/library/windows/desktop/ms632682) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 It does not destroy the `CWindow` object itself.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#5](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#5)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)