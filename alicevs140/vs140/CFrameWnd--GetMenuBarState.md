---
title: "CFrameWnd::GetMenuBarState"
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
ms.assetid: df3d9ec1-71fa-4ddb-bc51-c372b8ebf3bb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::GetMenuBarState
Retrieves the display state of the menu in the current MFC application.  
  
## Syntax  
  
```  
virtual DWORD GetMenuBarState();  
```  
  
## Return Value  
 The return value can have the following values:  
  
-   AFX_MBS_VISIBLE (0x01) – The menu is visible.  
  
-   AFX_MBS_HIDDEN (0x02) – The menu is hidden.  
  
## Remarks  
 If a runtime error occurs, this method asserts in Debug mode and raises an exception derived from the [CException](../vs140/CException-Class.md) class.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::SetMenuBarState](../vs140/CFrameWnd--SetMenuBarState.md)