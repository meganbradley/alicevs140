---
title: "CMDIChildWnd::MDIDestroy"
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
ms.assetid: 16d20d80-19ef-4cd1-8da5-1df9cf363ebd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWnd::MDIDestroy
Call this member function to destroy an MDI child window.  
  
## Syntax  
  
```  
  
void MDIDestroy( );  
```  
  
## Remarks  
 The member function removes the title of the child window from the frame window and deactivates the child window.  
  
## Example  
 [!CODE [NVC_MFCWindowing#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#10)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_MDIDESTROY](http://msdn.microsoft.com/library/windows/desktop/ms644914)   
 [CMDIChildWnd::Create](../vs140/CMDIChildWnd--Create.md)