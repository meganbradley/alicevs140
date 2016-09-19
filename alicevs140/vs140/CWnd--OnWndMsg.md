---
title: "CWnd::OnWndMsg"
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
ms.assetid: ef25c1da-717e-4a5a-a4ee-8e49c9adddd9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnWndMsg
This member function is called by `WindowProc`, or is called during message reflection.  
  
## Syntax  
  
```  
  
      virtual BOOL OnWndMsg(  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam,  
   LRESULT* pResult   
);  
```  
  
#### Parameters  
 `message`  
 Specifies the message to be sent.  
  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information.  
  
 `pResult`  
 The return value of [WindowProc](../vs140/CWnd--WindowProc.md). Depends on the message; may be **NULL**.  
  
## Return Value  
 **TRUE** if message was handled; otherwise **FALSE**.  
  
## Remarks  
 `OnWndMsg` determines the message type and either calls the appropriate framework function (for example, [OnCommand](../vs140/CWnd--OnCommand.md) for **WM_COMMAND**) or finds the appropriate message in the message map.  
  
 For more information about message reflection, see [Handling Reflected Messages](../vs140/Handling-Reflected-Messages.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnChildNotify](../vs140/CWnd--OnChildNotify.md)   
 [CWnd::SendChildNotifyLastMsg](../vs140/CWnd--SendChildNotifyLastMsg.md)   
 [CWnd::ReflectChildNotify](../vs140/CWnd--ReflectChildNotify.md)   
 [CCmdTarget::OnCmdMsg](../vs140/CCmdTarget--OnCmdMsg.md)   
 [CWnd::ReflectLastMsg](../vs140/CWnd--ReflectLastMsg.md)