---
title: "CMDIFrameWnd::MDISetMenu"
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
ms.assetid: 1cdd4e0e-896c-492a-88f3-aa625be69dd9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDISetMenu
Replaces the menu of an MDI frame window, the Window pop-up menu, or both.  
  
## Syntax  
  
```  
  
      CMenu* MDISetMenu(  
   CMenu* pFrameMenu,  
   CMenu* pWindowMenu   
);  
```  
  
#### Parameters  
 *pFrameMenu*  
 Specifies the menu of the new frame-window menu. If **NULL**, the menu is not changed.  
  
 `pWindowMenu`  
 Specifies the menu of the new Window pop-up menu. If **NULL**, the menu is not changed.  
  
## Return Value  
 A pointer to the frame-window menu replaced by this message. The pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 After calling `MDISetMenu`, an application must call the [DrawMenuBar](../vs140/CWnd--DrawMenuBar.md) member function of `CWnd` to update the menu bar.  
  
 If this call replaces the Window pop-up menu, MDI child-window menu items are removed from the previous Window menu and added to the new Window pop-up menu.  
  
 If an MDI child window is maximized and this call replaces the MDI frame-window menu, the Control menu and restore controls are removed from the previous frame-window menu and added to the new menu.  
  
 Do not call this member function if you use the framework to manage your MDI child windows.  
  
## Example  
 [!CODE [NVC_MFCWindowing#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#19)]  
  
 [!CODE [NVC_MFCWindowing#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#20)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DrawMenuBar](../vs140/CWnd--DrawMenuBar.md)   
 [WM_MDISETMENU](http://msdn.microsoft.com/library/windows/desktop/ms644921)