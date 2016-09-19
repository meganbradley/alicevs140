---
title: "CWindow::RedrawWindow"
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
ms.assetid: e67b722a-dd9a-46fa-a8e3-95c2e65ae84c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::RedrawWindow
Updates a specified rectangle or region in the client area.  
  
## Syntax  
  
```  
  
      BOOL RedrawWindow(  
   LPCRECT lpRectUpdate = NULL,  
   HRGN hRgnUpdate = NULL,  
   UINT flags = RDW_INVALIDATE | RDW_UPDATENOW | RDW_ERASE   
); throw()   
```  
  
## Remarks  
 See [RedrawWindow](http://msdn.microsoft.com/library/windows/desktop/dd162911) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#28](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#28)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::UpdateWindow](../vs140/CWindow--UpdateWindow.md)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)