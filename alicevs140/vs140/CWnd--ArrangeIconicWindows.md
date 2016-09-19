---
title: "CWnd::ArrangeIconicWindows"
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
ms.assetid: 4090855b-2436-4cba-9a17-ef4dc7e02973
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ArrangeIconicWindows
Arranges all the minimized (iconic) child windows.  
  
## Syntax  
  
```  
  
UINT ArrangeIconicWindows( );  
```  
  
## Return Value  
 The height of one row of icons if the function is successful; otherwise 0.  
  
## Remarks  
 This member function also arranges icons on the desktop window, which covers the entire screen. The [GetDesktopWindow](../vs140/CWnd--GetDesktopWindow.md) member function retrieves a pointer to the desktop window object.  
  
 To arrange iconic MDI child windows in an MDI client window, call [CMDIFrameWnd::MDIIconArrange](../vs140/CMDIFrameWnd--MDIIconArrange.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#66](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#66)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDesktopWindow](../vs140/CWnd--GetDesktopWindow.md)   
 [CMDIFrameWnd::MDIIconArrange](../vs140/CMDIFrameWnd--MDIIconArrange.md)   
 [ArrangeIconicWindows](http://msdn.microsoft.com/library/windows/desktop/ms632671)