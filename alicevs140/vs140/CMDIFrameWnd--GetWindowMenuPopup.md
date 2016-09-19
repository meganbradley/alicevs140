---
title: "CMDIFrameWnd::GetWindowMenuPopup"
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
ms.assetid: d65359cc-1d52-4467-9e02-27c15defad83
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::GetWindowMenuPopup
Call this member function to obtain a handle to the current pop-up menu named "Window" (the pop-up menu with menu items for MDI window management).  
  
## Syntax  
  
```  
  
      virtual HMENU GetWindowMenuPopup(  
   HMENU hMenuBar   
);  
```  
  
#### Parameters  
 *hMenuBar*  
 The current menu bar.  
  
## Return Value  
 The Window pop-up menu if one exists; otherwise **NULL**.  
  
## Remarks  
 The default implementation looks for a pop-up menu containing standard Window menu commands such as **ID_WINDOW_NEW** and **ID_WINDOW_TILE_HORZ**.  
  
 Override this member function if you have a Window menu that does not use the standard menu command IDs.  
  
## Example  
 [!CODE [NVC_MFCWindowing#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#16)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDIGetActive](../vs140/CMDIFrameWnd--MDIGetActive.md)