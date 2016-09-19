---
title: "CMDIFrameWnd::MDIActivate"
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
ms.assetid: 5dc97a6b-5880-4387-9b58-ad7914501cb0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDIActivate
Activates a different MDI child window.  
  
## Syntax  
  
```  
  
      void MDIActivate(  
   CWnd* pWndActivate   
);  
```  
  
#### Parameters  
 *pWndActivate*  
 Points to the MDI child window to be activated.  
  
## Remarks  
 This member function sends the [WM_MDIACTIVATE](../vs140/CWnd--OnMDIActivate.md) message to both the child window being activated and the child window being deactivated.  
  
 This is the same message that is sent if the user changes the focus to an MDI child window by using the mouse or keyboard.  
  
> [!NOTE]
>  An MDI child window is activated independently of the MDI frame window. When the frame becomes active, the child window that was last activated is sent a [WM_NCACTIVATE](../vs140/CWnd--OnNcActivate.md) message to draw an active window frame and caption bar, but it does not receive another `WM_MDIACTIVATE` message.  
  
## Example  
 See the example for [CMDIFrameWnd::GetWindowMenuPopup](../vs140/CMDIFrameWnd--GetWindowMenuPopup.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDIGetActive](../vs140/CMDIFrameWnd--MDIGetActive.md)   
 [CMDIFrameWnd::MDINext](../vs140/CMDIFrameWnd--MDINext.md)   
 [CWnd::OnActivate](../vs140/CWnd--OnActivate.md)   
 [WM_NCACTIVATE](http://msdn.microsoft.com/library/windows/desktop/ms632633)