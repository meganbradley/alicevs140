---
title: "CWindow::CenterWindow"
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
ms.assetid: f7d3543a-032b-4bbc-8e15-1f739e5c594e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::CenterWindow
Centers the window against a given window.  
  
## Syntax  
  
```  
  
      BOOL CenterWindow(  
   HWND hWndCenter = NULL   
) throw();  
```  
  
#### Parameters  
 `hWndCenter`  
 [in] The handle to the window against which to center. If this parameter is **NULL** (the default value), the method will set `hWndCenter` to the window's parent window if it is a child window. Otherwise, it will set `hWndCenter` to the window's owner window.  
  
## Return Value  
 **TRUE** if the window is successfully centered; otherwise, **FALSE**.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#4](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#4)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::MoveWindow](../vs140/CWindow--MoveWindow.md)   
 [CWindow::SetWindowPos](../vs140/CWindow--SetWindowPos.md)