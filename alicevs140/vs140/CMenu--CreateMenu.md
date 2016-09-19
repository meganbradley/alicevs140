---
title: "CMenu::CreateMenu"
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
ms.assetid: 8169d40c-fa14-4ff0-8c2b-b73e848a446e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::CreateMenu
Creates a menu and attaches it to the `CMenu` object.  
  
## Syntax  
  
```  
  
BOOL CreateMenu( );  
```  
  
## Return Value  
 Nonzero if the menu was created successfully; otherwise 0.  
  
## Remarks  
 The menu is initially empty. Menu items can be added by using the `AppendMenu` or `InsertMenu` member function.  
  
 If the menu is assigned to a window, it is automatically destroyed when the window is destroyed.  
  
 Before exiting, an application must free system resources associated with a menu if the menu is not assigned to a window. An application frees a menu by calling the [DestroyMenu](../vs140/CMenu--DestroyMenu.md) member function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#22)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::CMenu](../vs140/CMenu--CMenu.md)   
 [CMenu::DestroyMenu](../vs140/CMenu--DestroyMenu.md)   
 [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md)   
 [CWnd::SetMenu](../vs140/CWnd--SetMenu.md)   
 [CreateMenu](http://msdn.microsoft.com/library/windows/desktop/ms647624)   
 [CMenu::AppendMenu](../vs140/CMenu--AppendMenu.md)